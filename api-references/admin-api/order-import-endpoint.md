---
description: >-
  The endpoint offers a simplified way of importing orders into the shop, e.g.
  to transfer old orders from an ERP system.
---

# Order Import Endpoint

{% hint style="warning" %}
The Endpoint isn't available yet and will be released with the version 0.9.5 of the B2BSellers Core Plugin
{% endhint %}

{% hint style="success" %}
**Performance geek:** Without any performance-optimization, you can insert 250 Orders under one minute!
{% endhint %}

### Useful Links

{% content-ref url="../../developer-guides/guides-for-erp-interface/integration-of-erp-orders-to-shopware-6.md" %}
[integration-of-erp-orders-to-shopware-6.md](../../developer-guides/guides-for-erp-interface/integration-of-erp-orders-to-shopware-6.md)
{% endcontent-ref %}

### Changing default configuration options

To change any default configuration option, you have to make the change in the **b2b\_sellers\_core.yaml** file. You can place it in your Shopware installation under **config/packages/**.

```yaml
# config/packages/b2b_sellers_core.yaml
b2b_sellers_core:
  order_import:
    default_sales_channel_id: 3599498813f14f1a8abe0deb0e12d180
    default_currency_id: b7d2554b0ce847cd82f3ac9bd1c0dfca
    default_language_id: 2fbb5fe2e29a4d70aa5854ce7ce3e20b
```

The **default\_sales\_channel\_id** isn't set out of the box and has to be provided in every order if not configured.\
\
The **default\_currency\_id** isn't set out of the box and the currency id of the Shopware defaults (Defaults::CURRENCY) is used when not provided.\
\
The **default\_language\_id** isn't set out of the box and the language id of the Shopware defaults (Defaults::LANGUAGE\_SYSTEM) is used when not provided.\


{% hint style="info" %}
The default Ids can be overwritten by providing them in the order data
{% endhint %}

{% swagger method="post" path="api/_action/order-import" baseUrl="https://app.com/" summary="Importing orders" %}
{% swagger-description %}
Simplified endpoint for importing orders to Shopware
{% endswagger-description %}

{% swagger-parameter in="body" name="order" type="array" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Response without any errors" %}
```json
{
	"success": true,
	"errors": [],
	"result": [
		{
			"row": 0,
			"id": "054386a889de4f9b9f449e687112d955"
		}
	]
}
```


{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Response when errors occured" %}
```json
{
	"succes": false,
	"errors": [
		{
			"row": 0,
			"errors": [
				"Value is not a valid UUID: 3599498813f14f1a8abe0deb0e12d1801"
			]
		}
	],
	"result": []
}
```
{% endswagger-response %}
{% endswagger %}

### Endpoint request body

```json
{
  "orders": [
    {
      "salesChannelId": "3599498813f14f1a8abe0deb0e12d1801", // (required) if default not configured
      //"currency": "EUR", // ISO-Code or ID
      //"language": "de-DE", // Locale code or ID
      //"customer": "10000", // customerNumber or ID
      "orderCustomer": { 
        "customer": "10000", // customerNumber or ID
        "salutation": "mr" // salutationKey or Id
        "firstName": "string",
        "lastName": "string",
        "email": "string",
        ...(default optional fields)
      }, 
      "orderDateTime": "2022-01-01 06:00:00",
      "shippingDateEarliest": "2022-01-12 06:00:00",
      "shippingDateLatest": "2022-01-14 06:00:00",
      "orderNumber": "T1236", // (required) update if exists
      "deliveryStatus": "open", // delivery state technicalName
      "orderStatus": "open", // order state technicalName
      "paymentStatus": "open", // transaction state technicalName
      "shippingMethod": "Standard", // translated name
      "paymentMethod": "Invoice", // translated name
      "lineItems": [
        {
          "type": "product",
          "price": 14.875,
          "netPrice": 12.50, 
          "quantity": 1,
          "product": "SWDEMO10001", // productNumber or ID (required for product type)
          "label": "string", // (optional for product line items)
          "good": true, // (optional)
          "removable": true, // (optional)
          "stackable": true, // (optional)
          "position": 1, // (optional)
          "description": "string", // (optional)
          "payload": [], // (optional)
          "customFields": [], // (optional)
        }
      ],
      "shippingCosts": {
        "price": 4.99,
        "netPrice": 4.99
      },
      "billingAddress": {
        "salutation": "mr", // salutationKey or Id
        "firstName": "firstName",
        "lastName": "lastName",
        "street": "street",
        "zipcode": "zipcode",
        "city": "city",
        "country": "DE" // ID or ISO-Code
      }
      "shippingAddress": { // (optional: billingAddress used)
        // same es billingAddress 
      }
    }
  ]
}
```

#### Minimal example:

```json
{
  "orders": [
    {
      "salesChannelId": "3599498813f14f1a8abe0deb0e12d1801",
      "customer": "10000", 
      "orderDateTime": "2022-01-01 06:00:00",
      "shippingDateEarliest": "2022-01-12 06:00:00",
      "shippingDateLatest": "2022-01-14 06:00:00",
      "orderNumber": "T1236",
      "deliveryStatus": "open",
      "orderStatus": "open", 
      "paymentStatus": "open",
      "shippingMethod": "Standard",
      "paymentMethod": "Invoice",
      "lineItems": [
        {
          "type": "product",
          "price": 14.875,
          "netPrice": 12.50,
          "quantity": 1,
          "product": "SWDEMO10001"
        }
      ],
      "shippingCosts": {
        "price": 4.99,
        "netPrice": 4.99
      },
      "billingAddress": {
        "salutation": "mr",
        "firstName": "firstName",
        "lastName": "lastName",
        "street": "street",
        "zipcode": "zipcode",
        "city": "city",
        "country": "DE"
      }
    }
  ]
}
```

### Request body explanation

#### **Price**

Taxes are calculated automatically.\
The overall order price is being calculated by the prices from line items and shipping costs.

#### Customer

The endpoint provides serveral options for the order customer data

* The orderCustomer array can be generated by the endpoint when the customerId or the customerNumber are given in the "customer" field.
* The orderCustomer can be provided normally and the customerId can't be fetched by providing the customerNumber inside of the orderCustomer array in the "customer" field.

#### Salutations

Salutations are accepted as Id or salutation key (e.g. mr,...)

#### States

States for order, delivery and transaction have to be the technical name of the state
