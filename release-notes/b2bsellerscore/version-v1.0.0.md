---
description: 'Release date: 24.01.2023'
---

# Version v1.0.0

## Release Notes

{% hint style="info" %}
Here you'll find our Blog post with detailed description and developer infos: \
\
DE => [https://www.b2b-sellers.com/de/release-news-produkt-updates-im-januar-2023/](https://www.b2b-sellers.com/de/release-news-produkt-updates-im-januar-2023/)\
... or ... \
EN => [https://www.b2b-sellers.com/en/release-news-product-updates-january-2023/](https://www.b2b-sellers.com/en/release-news-product-updates-january-2023/)
{% endhint %}

**Issues**\
BCS-32 Provide a migration so that all customers become B2B platform customers\
BCS-721 Enabling the bonus configurations for administrators of a company\
BCS-778 Budget resets automatically when daily, quarterly, yearly time reached\
BCS-850 The B2B-Platform Menu is now editable under Admin > B2B settings\
BCS-870 Error/Sucess Message after creating a new user by registration Link added\
BCS-988 fixed notice for customer, if discount rate is active and customer specific price is availible, that the discount rate is not applied to a customer specific price\
BCS-992 Removed duplicate customer creation for the storefront registration\
BCS-1010 Add all languages to command b2b:platform-menu:rebuild\
BCS-1053 Implemented lots of Cypress E2E Tests - (happy path) + Codeception Integrations Tests for testing the Store-API routes\
BCS-1089 Options added for global reachable categories in the  "[B2bPartialAssortments](../../user-guide/configuration-of-purchasable-addons/customer-specific-assortments.md)" addon settings\
BCS-1044 Successfully tested on Shopware Version 6.4.17.\*\
BCS-1069 Successfully tested on Shopware Version 6.4.18.\*

**New Features**\
BCS-250 Provide a employee Upload via CSV-File\
BCS-1054 new Addon available "[B2bPartialAssortments](../../user-guide/configuration-of-purchasable-addons/customer-specific-assortments.md)" - Enable customer-specific assortments\
BCS-1052 Added the [OCI-Punchout](../../user-guide/configuration-of-purchasable-addons/e-procurement-oci-punchout.md) as purchaseable addon to B2BsellersCore\
BCS-1073 Added the [cXML/Ariba-Punchout](../../user-guide/configuration-of-purchasable-addons/e-procurement-cxml-purchase-order-ariba.md) as purchaseable addon to B2BsellersCore

**Bugs**\
BCS-553 On b2b:customer:migrate Command, check if customer-group names are available\
BCS-605 Verification and prohibition of logins in relation to B2B customer, sales representative & B2C customer\
BCS-815 Added getter and setter methodes for all Translation Entity Classes\
BCS-827 Saleschannel binding to employees\
BCS-839 If no salutation is stored for an address and you get a message in the shopping cart, a pop-up opens directly in which you can configure the salutation.\
BCS-844 Renaming "Quick oder" in to "Fast order"\
BCS-845 Menu tab "Order templates" is hidden when plugin is inactive and renamed to "Order Lists"\
BCS-855 disable "Not specified" in salutation on employee edit page\
BCS-995 Discount-Rate Notification on product detailpage is not shown + allowEmpty on product -> max discountRate and customer -> discountRate\
BCS-996 after update to 0.9.6 product request form is not showing on product detail page\
BCS-999 Product request form shows no error-message when recipient is not configured\
BCS-1000 Fast order won\`t be send from sales rep\
BCS-1002 Headline typo fixed in B2Bsellers Platform Menu - Shopware Admin settings\
BCS-1005 Reset of the "per order" budget after order is send\
BCS-1007 Fixed add employee form - add employee from customerlist overview\
BCS-1009 Fixed comment on offer request from product detail page is not showed in order\
BCS-1016 For best performer show only orders of current year and add variable to snippet\
BCS-1017 Fixed missing item numbers in customer dashboard -> ordered items\
BCS-1018 Private product list should only visible for that employee, changed private order template? to => private\
BCS-1021 Fixed usage of Express-Checkout Address Settings\
BCS-1022 Fixed net price displayed at offer overview\
BCS-1025 Fixed url\`s to new documentation structure in Plugin configurations\
BCS-1026 Fixed naming and description of PDP variant and order list inclusive features in Admin\
BCS-1028 Fixed employee import via csv functionallity\
BCS-1029 Fixed bin/console b2b:product-subscription:order command\
BCS-1031 Removed option to delete or edit a budget as employee\
BCS-1033 Fixed copper brass surcharge price calculation\
BCS-1034 Added/fixed missing exploded view optional field translation\
BCS-1035 Added more spacing between buttons of request offer and add to orderlists on PDP\
BCS-1036 Fixed on request form to not take companyName of active billing addres\
BCS-1039 When B2bProductLists/OrderLists is inactive don't navigation for orderlists under products in b2bplatform\
BCS-1041 Hide product prices in non-logged-in state, if hide product prices is set in settings\
BCS-1047 add admin to form on employee create at administration for customer\
BCS-1048 Removed payment condition from customer b2b specifications (customer fields)\
BCS-1051 Custom article item not showing on order detail on administration\
BCS-1055 Auto-Login settings for sales representative (Login with hash) in administration\
BCS-1061 Added missing customField for url authentication hash on employee details (administration)\
BCS-1085 Fixed npm errors on b2b:platform:build command\
BCS-957 Product comment in offer not visible
