---
description: 'Release date: 03.05.2023'
---

# Version v1.0.4

Release Notes

{% hint style="info" %}
Here you'll find our Blog post with detailed description and developer infos: \
\
DE => [https://www.b2b-sellers.com/de/b2bsellers-suite-1-0-4/](https://www.b2b-sellers.com/de/b2bsellers-suite-1-0-3/)\
... or ... \
EN => [https://www.b2b-sellers.com/en/b2bsellers-suite-1-0-4/](https://www.b2b-sellers.com/en/b2bsellers-suite-1-0-3/)
{% endhint %}

**Issues**\
BCS-1224 Sucessfully tested with Shopware 6.4.20.1\
BCS-1243 Created an exception if no B2BPlatform menu is stored in the core settings.\
BCS-1239 New minimum Shopware Version in Composer set to 6.4.20\
BCS-1241 Added alert for "Send Welcome Mail with Password activation" on employee detail when employee has no assigned customers and disable action button\
BCS-1256 Criteria improvements for SalesRepresentativeRoute\
BCS-1257 Added ActivateB2bSellersAddonEvent/DeactivateB2bSellersAddonEvent to the addon/feature toggling\
BCS-1259 Removed node\_modules from custom/plugins/b2bsellerscore/src/Resources/app/administration\
BCS-1088 Added Presettings for B2Bsellers Suite config fields

**New Features**\
BCS-1095 Time limited customised prices added\
BCS-1163 add "clear all filters" to vue.js b2b-platform table component if filtered and 0 results\
BCS-1209 Splitted global and customer specific roles in B2BPlattform - Storefront\
BCS-1215 Added all B2Bsellers Suite Entity Custom Fields into Admin > Settings > Custom Field > Assign to Entity\
BCS-1228 Added contact details of employees on sales rep. overview\
BCS-1230 Created Store-API for Variant-List data to product detail page, replaced in ProductListSubscriber.php

**Bugs**\
BCS-1169 Fixed price recalculation of manuall changed prices from private to business view (Gross/Net)\
BCS-1221 Fixed the bonus credit is not deducted after redeeming\
BCS-1222 Fixed creation of orderlists method type private\
BCS-1223 Fixed login into preferred company with individual login link\
BCS-1225 Fixed error message on csv fast order\
BCS-1226 Fixed order list widget on Cockpit when function is disabled\
BCS-1229 Fixed required field currency at customer specific prices\
BCS-1231 Fixed "display error" in company selection when the customer's company name is empty\
BCS-1233 Fixed redirect of account activation page on ResponseSubscriber by refactoring whitelists\
BCS-1238 Fixed pricefilter option was not hidden with disabled priceview\
BCS-1240 Added employee permission group + translation table to uninstall method of B2bSellersCore.php\
BCS-1242 Fixed attached trade confirmation on registration form was not submitted by mail\
BCS-1245 Fixed issue that you can log in as B2B Customer, although there are employees.\
BCS-1248 Fixed dump in OrderStateChangedSubscriber.php\
BCS-1249 Fixed order list item calculation over whole assortment when no item is in the order list\
BCS-1251 Fixed redirect on closed shops and 404 handling on failure\
BCS-1258 Fixed that employee can edit addresses although the role does not allow it\
BCS-1252 Fixed criteria to show correct order lists



