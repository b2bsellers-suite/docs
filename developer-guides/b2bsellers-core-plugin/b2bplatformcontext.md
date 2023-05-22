# B2bPlatformContext

## **What is the B2bPlatformContext?**

In the Shopware standard there is already the normal SalesChannelContext, we have extended this via the "extension" accordingly with a new b2BPlatformContext to provide B2B-specific data in the user context.

#### Examples:

* Which employee of a "customer" is logged in?
* Is a sales employee logged in? And is he currently logged in to a customer.
* Is the employee an admin or not?
* Which employee with which role is logged in?

The b2bPlatformContext is available from anywhere. (Can be accessed from anywhere.)

#### **Example:**

![Figure 1. This B2BPlatform Context shows that the user is an employee of a client (isEmployee: true).](<../../.gitbook/assets/example - B2BPlatformContext.png>)

<div align="left">

<img src="../../.gitbook/assets/example - B2BPlatformContext 2.png" alt="Figure 2 - This B2bPlatformContext shows a loggedin sales representative who has not yet logged in to a customer employee.">

</div>

#### **Note alert**

the B2BplatformContext is only set when you are logged in as, so we always recommend asking beforehand.

```
if(!$context->hasExtension('b2bPlatformContext')) {
return; 
}
```

Alternatively, the B2BPlatformContext can always be requested via the B2bContextTrait (see documentation [b2bcontexttrait.md](b2bcontexttrait.md "mention")).

![](<../../.gitbook/assets/example - B2BPlatformContext 3.png>)

#### Note Alert:

In the employeeCustomer is the connection table between the logged-in employee and the assigned customer. The role, admin, etc. are maintained here.

#### Examples:

<div align="left">

<img src="../../.gitbook/assets/example - B2BPlatformContext 4.png" alt="Figure 3. Here will be checked whether the logged-in user is a sales employee.">

</div>

![Figure 4: Here, the logged-in employee will be queried via the B2bPlatformContext. Notice. These are the general employee data, not the employees ->mapping -> Customer data.](<../../.gitbook/assets/example - B2BPlatformContext 5.png>)
