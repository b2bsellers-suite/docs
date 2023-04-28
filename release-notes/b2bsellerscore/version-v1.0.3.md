---
description: 'Release date: 05.04.2023'
---

# Version v1.0.3

Release Notes

{% hint style="info" %}
Here you'll find our Blog post with detailed description and developer infos: \
\
DE => [https://www.b2b-sellers.com/de/b2bsellers-suite-1-0-3/](https://www.b2b-sellers.com/de/b2bsellers-suite-1-0-3/)\
... or ... \
EN => [https://www.b2b-sellers.com/en/b2bsellers-suite-1-0-3/](https://www.b2b-sellers.com/en/b2bsellers-suite-1-0-3/)
{% endhint %}

**Issues**\
BCS-991 show pseudo price on custom specific prices as strike price on product detail page\
BCS-1143 Added the company name to B2B registration forms (closed shop)\
BCS-1172 Changed output of the variant list on the product detail page after the item description\
BCS-1188 Refactoring of the ResponseSubscriber\
BCS-1189 Added new default routes to whitelist for closed shops

**New Features**\
BCS-1184 Complete headless-approach \[Store-API Routes instead of Subscriber Methods]

**Bugs**\
BCS-605 Verification and prohibition of logins in relation to B2B customer, sales representative & B2C customer\
BCS-1183 Fixed provide employee data in status update email context\
BCS-1185 Fixed random employee logout behaviour\
BCS-1186 Fixed limited available customers in assign new company dropdown\
BCS-1187 Fixed passwordless login on closed shops\
BCS-1190 Refactoring of the SalesChannelContextPersisterDecorater for B2Bcontext\
BCS-1191 Fixed autocomplete dropdown at fast order form\
BCS-1192 Fixed dashboard items without a picture tried to load whole media catalog\
BCS-1194 Fixed passwordless login via e-mail link\
BCS-1199 Fixed function enrichProductListEntities for orderlists\
BCS-1200 Fixed not showing products list switcher even with filled customFields on category\
BCS-1201 Fixed recursion for store-api/category on CategoryRouteDecorator\
BCS-1202 Fixed welcome mail content to SalesChannel binding of the employee\
BCS-1203 Fixed delete customer assortements info when customers connected\
BCS-1104 Fixed products shown in Quick Order even if they shouldn\`t from customer assortements
