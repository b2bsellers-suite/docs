---
description: 'Release date: 03.07.2023'
---

# Version v1.1.1

Release Notes

{% hint style="info" %}
Here you'll find our Blog post with detailed description and developer infos: \
\
DE => [https://www.b2b-sellers.com/de/b2bsellers-release-1-1-1/](https://www.b2b-sellers.com/de/b2bsellers-release-1-1-1/)\
... or ... \
EN => [https://www.b2b-sellers.com/en/b2bsellers-release-1-1-1/](https://www.b2b-sellers.com/en/b2bsellers-release-1-1-1/)
{% endhint %}

**Issues**\
BCS-1278 Add Fallback translation if language value isn’t set\
BCS-869 Added command to reinstall or overwrite email templates\
BCS-1078 now all js files of the addons are built at the b2b:platform:build, before only the active addons were built. In the UI only the active addon js \\(Storefront/Admin/B2B-Platform\\) are loaded.\
BCS-1179 Event Items available for clearance requests\
BCS-1232 Splitted the AbstractEmployeeRoute to seperate „Invite“ and „Export“ Routes\
BCS-1236 Added admin config for „The following status influence the number of participants“\
BCS-1196 Improved participant details\
BCS-1260 Replace customer.company to customer.displayName and added EntityExtension for displayName\
BCS-1303 in the „b2b:platform:build“ command check if the build process was successful, otherwise return 1, so that CI pipelines can react to it\
BCS-1311 Added PlatformProductSearchCriteriaEvent to the PlatformProductSearchRoute\
BCS-1330 Added ApiAware flag to the Id field of the B2bProductListTypeDefinition\
BCS-1352 Moved Event article fields from B2B Specifications to Shopware standard custom fields\
BCS-698 Added a „price changed“ badge to customer cart when proce was adjusted by salerep\
BCS-740 Added information of the employee, who added the product to the cart\
BCS-1121 Added Waiting list function for the Event manager\
BCS-1198 Added customer specific caching for system relevant routes\
BCS-1279 Added location on Event Detail Page\
BCS-1287 Added recipient information to orders for status update emails\
BCS-1288 Added employee name to orders\
BCS-1293 Added Eventname to the appointment overview\
BCS-1091 Added CSV upload to orderlists

**New Features**\
BCS-698 Added a "price changed" badge to customer cart when proce was adjusted by salerep BCS-740 Added information of the employee, who added the product to the cart \
BCS-1121 Added Waiting list function for the Event manager \
BCS-1198 Added customer specific caching for system relevant routes \
BCS-1279 Added location on Event Detail Page \
BCS-1287 Added recipient information to orders for status update emails \
BCS-1288 Added employee name to orders \
BCS-1293 Added Eventname to the appointment overview \
BCS-1091 Added CSV upload to orderlists

**Bugs**\
BCS-736 Fixed locale dependent platform datetime spelling \
BCS-1103 Fixed Abo-Items in customer cart salerep view and offer functions \
BCS-1118 Fixed gross/net price on orderlist view \
BCS-1176 Fixed handling for orderlist and offers when a product is deleted \
BCS-1213 Fixed that the b2b:platform:watch gave a header error when a closed store is selected in the plugin config. \
BCS-1238 Fixed pricefilter option was not hidden with disabled priceview \
BCS-1265 Fixed customer specific prices – validation of price field typ – working without from – to range again \
BCS-1271 Fixed LineItemCommentSubscriber for console handling \
BCS-1281 Fixed bug when during login the employee isn’t a admin and has no role \
BCS-1286 Fixed event registration with full occupancy and booking in the shopping cart \
BCS-1289 Fixed lineItem handling with additional pseudo product plugin \
BCS-1292 Fixed custom field filters for activity log \
BCS-1294 Fixed calculation of total offer sum when subscription Items are added \
BCS-1295 Fixed deprecated LoginAsCustomer method \
BCS-1296 Removed „footer.serviceHotline“ Snippet \
BCS-1297 Fixed only sales channel specific customers on offer creation \
BCS-1299 Fixed advanced pricing won’t show on search results with a single product as search result \
BCS-1300 Fixed 404 redirect on not existing url call \
BCS-1301 Fixed error message on B2Bsellers closed shop login form \
BCS-1304 Fixed error message on profile page password change \
BCS-1305 Fixed password reset link in mail on salesChannel base \
BCS-1306 Fixed missing margin when creating the offer as a sales representative. \
BCS-1308 Fixed missing theme snippets in the snippet route \
BCS-1309 Fixed locale dependent platform currency spelling \
BCS-1312 Fixed problem with creating a orderlist from the PDP \
BCS-1322 Fixed local dependent datetime spelling on the PDP \
BCS-1323 Fixed swapped language DK and PL in Migration \
BCS-1325 Fixed item limit of 100 countrys at offers and addresses dropdowns \
BCS-1326 Fixed missing translation in B2B Platform Menu \
BCS-1328 Fixed missing translation for „Opt.“ at offer-item-list/template.html.twig \
BCS-1331 Fixed category extension for the cms page in the CategoryRouteDecorator \
BCS-1332 Fixed problems when adding a product to a orderlist fails on orderlist creation from the PDP or category view \
BCS-1337 Fixed Update error on V1.1.0 when language is missing \
BCS-1340 Fixed only statistics and activitys from assigned customers is visible for sales representive in his dashboard \
BCS-1345 Fixed category menu level settings when logged in into B2Bsellers Suite



