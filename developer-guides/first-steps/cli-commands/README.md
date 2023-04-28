---
description: 'all available command are listed over bin/console and prefix b2b:'
---

# CLI-Commands

you can use following CLI Commands:

## B2bSellersCore

### B2B-Platform Build-Command (Vue.Js)

Following command build the Vue.js b2b-platform and make it available for production use.

```
bin/console b2b:platform:build
```

### Entity-Mapping Command&#x20;

E.g. at the customer prices, it is possible to fill customer prices with customer numbers and product numbers instead of UUIDs. Following command fill the necessary UUIDs for product UUIDand customer UUIDif the product or customer is available.&#x20;

```bash
bin/console b2b:entity:map
```

{% hint style="info" %}
we recommend this as cronjob every 1 or 5 minutes&#x20;
{% endhint %}

### Migrate existing customers to B2B-customers & create first employee for all available b2b-customers

If you setup our B2Bsellers to an existing shopware 6 shop, you might want all customers to be created directly as employees, so that the login remains and they are forwarded directly to the B2B platform. Then the following commands makes sense for you. Please check on a local environment which command makes sense.

```
// work through for migrating a normal shopware customer to a b2bplatform customer by filters and options.
bin/console b2b:migrate:customers

// create first employee (same data as customer) for all shopware-customers with custom field "b2b_platform_access" == true
bin/console b2b:create:first-employee-for-customer

// This command deletes all employees for the customers and resets all b2b custom fields for all customers
bin/console b2b:reset:customer
```

### Reinstall Custom Fields&#x20;

```
// Installs the CustomFields for Sales Representatives, Customers, Orders, ..
bin/console b2b:migrate:custom-fields
```

### Rebuild the B2B Platform Menu&#x20;

If you want to reset the B2B platform menu to the default, you can do this with this CLI command.

```
bin/console b2b:platform-menu:rebuild
```

## Create Test-Data

Currently, it creates only customer and employee test-user, but further, we want to create test products for each function

{% content-ref url="../../../user-guide/setup/test-daten.md" %}
[test-daten.md](../../../user-guide/setup/test-daten.md)
{% endcontent-ref %}

```
b2b:create:test-data
```

{% hint style="info" %}
please ensure, that your mail client is disabled.&#x20;
{% endhint %}

## B2bProductSubscriptions

Following command checks whether there are subscriptions for which an order must be triggered.

```
bin/console b2b:product-subscription:order
```
