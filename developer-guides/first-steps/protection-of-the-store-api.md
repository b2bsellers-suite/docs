# Protection of the Store-API

For IT security, it is important that the APIs are secure. As we have moved many functions to the Store API for the B2B platform, we have made functions ready to help you ensure that the API is secure.

## "Field" Protection in EntityDefinition

Some fields should be editable, some fields should only be editable **by themselves**, some fields should only be viewable by themselves or by a Sales representative.&#x20;

We have provided our own protection options for precisely these use cases, similar to the "_ApiAware()_" function of Shopware, and have built them into all current fields in a sensible way.

**Available Flags**

* CustomerWriteProtected()
* EmployeeReadProtected(true, \['admin'])
* EmployeeReadProtected(true)
* CustomFields -> EmployeeJsonWriteProtected()
* CustomFields -> EmployeeJsonReadProtected()

#### Examples:

```php
// you'll see this field as employee, if your are the admin of the customer

(new BoolField('isExternalEmployee', 'is_external_employee'))->addFlags( // this field is an example
    new ApiAware(),  
    new EmployeeReadProtected(true, ['admin']) // true means: read by himself allowed, but only if the employee has the role "Admin"
)
```

#### Protection of AssosciationFields

```php
// See Example Customer Write Protection and EmployeeReadProtection
(new ManyToOneAssociationField('preferredCustomer','preferred_customer_id',EmployeeCustomerDefinition::class,'id'))->addFlags(
      new ApiAware(),
      new CustomerWriteProtected(),
      new EmployeeReadProtected(true) // selfAllowed == true means that the employee himself can read this field
)
```

#### Protection of Custom Fields

```php
// If you want protect Custom Field Fields, then use this in your definition
// the second param is "selfAllowed", that means that you by yourself can update/read this field, but no other employee no matter if there is in your company
(new CustomFields())->addFlags(
    new ApiAware(),
    new EmployeeJsonWriteProtected(['b2b_url_login_authentication_hash'], true),
    new EmployeeJsonReadProtected(['b2b_url_login_authentication_hash'], true)
)
```

{% hint style="info" %}
We recommend using the protections especially for **association fields** in order not to display too much data to the client.
{% endhint %}

## Store-API Routes Protection

There are routes that only Sales representatives may request or routes that only B2B customers may request. However, **you must ensure this protection yourself in the STORE API**.

However, we would like to give you a few lines of sample code so that you can use them as a ready-to-use example.&#x20;

{% hint style="info" %}
**You can always use our traits here to query the B2BPlatformContext etc..**\
[**More Informations about the B2bContextTrait**](../b2bsellers-core-plugin/b2bcontexttrait.md)
{% endhint %}

### Add Route Annotations

#### B2bPlatformContextRequired

{% code lineNumbers="true" %}
```phpdoc
/**
    * @Entity("b2b_employee_customer")
    * @LoginRequired()
    * @B2bPlatformContextRequired()
    * @Route("/store-api/employee-customers", name="store-api.employee-customer.list", methods={"POST"})
*/
```
{% endcode %}

### Add Filter to the Criteria

You know that you can give your own criteria from the storefront through the request. This means that you could also request data from other employees or customers, which is why it is very important that you add filters yourself in the route and therefore overwrite any Store API criteria.&#x20;

If you **addFilter=> employeeId** from the B2BPlatformContext in the route, the filter on employeeId will be overwritten in any case! No matter what the visitor enters for employeeId in the frontend.

```php
// add Filter if customer is not an sales representative
if (!$this->customerIsSalesRepresentative($context)) {
    $criteria->addFilter(new EqualsFilter('employeeId', $this->getEmployee($context)->getId()));
}
```

More Examples:

```php
    /**
     * @Entity("b2b_employee_customer")
     * @LoginRequired()
     * @B2bPlatformContextRequired()
     * @Route("/store-api/employees", name="store-api.employee.list", methods={"POST"})
    */
    
    public function list(Request $request, SalesChannelContext $context, Criteria $criteria): EmployeeListResponse
    {
        if (!$this->customerIsSalesRepresentative($context)) {
            $criteria->addFilter(new EqualsFilter('customerId', $context->getCustomer()->getId()));
        }

        $criteria->addAssociation('employee');

        return new EmployeeListResponse(
            $this->employeeCustomerRepository->search($criteria, $context->getContext())
        );
    }
```

{% hint style="info" %}
If a "different" customerID" is already transferred **from the request criteria**, the appropriate login customer ID is automatically transferred here and thus there would be no output as a return, because there is no data record that has customerId == request-> criteria and customerId == route->criteria.
{% endhint %}

