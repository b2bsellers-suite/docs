# Migration of existing Shopware Customers

1. Integration into existing shopware 6 web shop\
   If you are already running a Shopware 6 shop, the only thing missing is the employee login for each customer and you have to fill in a custom field for the customer, which states that he has access to the B2B platform.\
   To migrate your existing customers, you can use a console command provided by us.

```
bin/console b2b:migrate:customers
```

You will go through a few questions so that an appropriate migration can then be made.

#### Example:

1. Should the first employee be created for migrated customers?
2. Should only customers with a filled company field be migrated?
3. Should customers with a specific email domain become a sales representative?
4. should only customers in special groups be migrated? \
   (You need to insert the name of the customer group separately with seminokol)

after the migration, all customers has one employee with the exact same mail address and from now on the employee logs in instead of the customer.

2\. Migration from Shopware Default Customer to B2B Customers with Platform Access

You can either run point 1. or the following console command:

```
b2b:create:first-employee-for-customer
```

This command automatically turns all customers who have "customFields > b2b\_platform\_access" to TRUE into a first employee with the exact same address, first name, last name and email address.

{% hint style="warning" %}
Please always test the commands in a development environment and never in a production environment.
{% endhint %}

#### Example process to migrate customers to b2b-customers

![](<../../../.gitbook/assets/image (131).png>)
