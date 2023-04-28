# EmployeePermissionTrait

Please have a look at the [B2BContextTrait](b2bcontexttrait.md) first.

## **Why is the EmployeePermissionTrait useful for your individual extension?**

With the EmployeePermissionTrait you can easily check in your PHP code whether the logged-in employee has the required rights.

### What are the possible functions:

<table><thead><tr><th>Function</th><th>Description</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td><code>checkB2bPlatformPermission</code></td><td>Check the permission of an employee:<br><br><strong>Example code:</strong><br><code>$this->checkB2bPlatformPermission([Permissions::</code><em><code>EMPLOYEE_PERMISSION_VIEW_ALL_ORDERS</code></em><code>], $context);</code></td><td></td><td></td></tr><tr><td><code>getEmployeeRole</code></td><td><p>Return of the EmployeeRoleEntity, if a role is stored accordingly.<br><br><strong>Example:</strong> </p><p><code>$role= $this->getEmployeeRole($context);</code><br><br></p></td><td></td><td></td></tr></tbody></table>

{% hint style="info" %}
Note (Alert): You must always pass the SalesChannelContext as a parameter.\
How to use the trait, please see the [B2BContextTrait.](b2bcontexttrait.md#note-alert)
{% endhint %}
