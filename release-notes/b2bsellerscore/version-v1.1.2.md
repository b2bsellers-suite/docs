---
description: 'Release date: 25.08.2023'
---

# Version v1.1.2

Release Notes

{% hint style="info" %}
Here you'll find our Blog post with detailed description and developer infos: \
\
DE => [https://www.b2b-sellers.com/de/b2bsellers-release-1-1-2/](https://www.b2b-sellers.com/de/b2bsellers-release-1-1-2)\
... or ... \
EN => [https://www.b2b-sellers.com/en/b2bsellers-release-1-1-2/](https://www.b2b-sellers.com/en/b2bsellers-release-1-1-2/)
{% endhint %}

**Issues**\
BCS-1278 Add Fallback translation if language value isn't set \
BCS-869 Added command to reinstall or overwrite email templates \
BCS-1078 now all js files of the addons are built at the b2b:platform:build, before only the active addons were built. In the UI only the active addon js (Storefront/Admin/B2B-Platform) are loaded. \
BCS-1179 Event Items available for clearance requests \
BCS-1232 Splitted the AbstractEmployeeRoute to seperate "Invite" and "Export" Routes \
BCS-1236 Added admin config for "The following status influence the number of participants" BCS-1196 Improved participant details \
BCS-1260 Replace customer.company to customer.displayName and added EntityExtension for displayName \
BCS-1303 in the "b2b:platform:build" command check if the build process was successful, otherwise return 1, so that CI pipelines can react to it \
BCS-1311 Added PlatformProductSearchCriteriaEvent to the PlatformProductSearchRoute \
BCS-1330 Added ApiAware flag to the Id field of the B2bProductListTypeDefinition \
BCS-1352 Moved Event article fields from B2B Specifications to Shopware standard custom fields

**New Features**\
BCS-1255 Added notice on b2b-platform > order lists as sales rep, if the order lists is only visible by sales rep. \
BCS-1335 Added CSV Export of participants to the Eventmanger \
BCS-1346 Added participant informations on order overview \
BCS-1366 Added a CSV Export to customer specific price overview in the storefront \
BCS-1367 Added time related columns to customer specific price view in the storefront

**Bugs**\
BCS-1253 Fixed customer specific prices handling for multiple prices with same specifications \
BCS-1282 Fixed flow trigger snippets in administration for all B2Bsellers flows \
BCS-1339 Fixed PdpVariantSettings Error on save \
BCS-1347 Fixed Indication of the number of participants \
BCS-1348 Fixed error message for InvalidEventLineItemTypeError \
BCS-1349 Fixed price editing of event items by sales rep. in customer cart \
BCS-1353 Fixed add to cart with hidden prices when not logged in \
BCS-1360 Fixed missing customer company name at order overview in admin \
BCS-1362 Fixed show up Eventarticle settings at product only when Eventmanager addon is active \
BCS-1363 Fixed registration with same email on different saleschannels \
BCS-1365 Fixed missing translation for customer specific price table \
BCS-1368 Fixed email template to sales rep on offer request \
BCS-1369 Fixed gross/net price on mulitple views \
BCS-1373 Fixed CSV Import to Orderlists \
BCS-1378 Fixed missing customer details block at order overview in admin \
BCS-1384 Fixed customer search route when a sales representative has assigned customers (/store-api/customer-search) \
BCS-1390 Fixed guest customer orders



