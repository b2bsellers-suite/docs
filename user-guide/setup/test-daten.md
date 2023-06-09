---
description: The B2B platform has the possibility to provide test data.
---

# Use Test-Customers

## Installation

Use the following console command to install the test data:

```
bin/console b2b:test-data:create
```

Since version 1.1.0 you can no longer create the test data directly in b2bsellercore but have to download a separate https://github.com/b2bsellers-suite/B2bDemodataPlugin for this purpose. With this additional plugin you can create more test data than before. Customers, employees, products and more.

How can you install the test data plugin? Run bin/console b2b:test-data:install-plugin or download the plugin as a ZIP file directly from Github and install it as a plugin. 2. after that you have new CLI commands available:

```
bin/console b2b:test-data:create // create all test-data
bin/console b2b:test-data:reset -f // delete all test-data
```

With these two commands you can now create or delete test data.

Download: [https://github.com/b2bsellers-suite/B2bDemodataPlugin ](https://github.com/b2bsellers-suite/B2bDemodataPlugin)

## Overview

### Sales Agent



**Shop operator**\
**Luxon Blech-Handel**\
www.luxon.com

<table><thead><tr><th></th><th>Sales staff (office)</th><th>Sals staff (field)</th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Customer no:</strong> </td><td>4771</td><td>4712</td><td></td></tr><tr><td><strong>Name:</strong></td><td>Michael Sommer</td><td>Markus Bauer</td><td></td></tr><tr><td><strong>User:</strong></td><td>m.sommer@luxon.de</td><td>m.bauer@luxon.de</td><td></td></tr><tr><td><strong>Password:</strong></td><td>b2bsellers</td><td>b2bsellers</td><td></td></tr><tr><td><strong>Role:</strong></td><td>Supervisor (all rights)</td><td>Access to two assigned employees</td><td></td></tr><tr><td></td><td><a href="https://luxon.demo.b2b-sellers.com/login/email/m.sommer@luxon.de/hash/vertriebsmitarbeiter"><mark style="color:blue;">Jetzt testen ></mark></a></td><td><a href="https://luxon.demo.b2b-sellers.com/login/email/m.bauer@luxon.de/hash/vertriebsmitarbeiter"><mark style="color:blue;">Jetzt testen ></mark></a></td><td></td></tr></tbody></table>

### Test customer EKTEK

#### customer

<table><thead><tr><th width="250">Ektek GmbH</th><th width="226">Ektek Spare-Parts GmbH</th><th>Ektek Training Center GmbH</th><th>Ektek Hausgeräte GmbH</th></tr></thead><tbody><tr><td>Customer no: 10002</td><td>Customer no: 10003</td><td>Customer no: 10005</td><td>Customer no. 10004</td></tr><tr><td><strong>Address:</strong></td><td><strong>Address:</strong></td><td><strong>Address:</strong></td><td><strong>Address:</strong></td></tr><tr><td>Ektek-Platz 1,<br>97070 Würzburg,<br>Germany</td><td>Dölitzerstr. 8,<br>04277 Leipzig,<br>Germany</td><td>Stadtweg 34,<br>90453 Nürnberg,<br>Germany</td><td>Dölitzerstr. 8,<br>04277 Leipzig,<br>Germany</td></tr><tr><td>info@ektek.com</td><td>info@ektek-ersatzteile.com</td><td>info@ektek-training-solution.com</td><td>info@ektek.com</td></tr><tr><td><strong>Alternative delivery address:</strong></td><td><strong>Alternative delivery address:</strong></td><td><strong>Alternative delivery address:</strong></td><td></td></tr><tr><td>Königsbergerstr. 19A ,<br>25421 Pinneberg,<br>Germany</td><td>Donaustr. 9,<br>15827 Blankenfelde-Mahlow,<br>Germany</td><td>Donaustr. 9,<br>15827 Blankenfelde-Mahlow,<br>Germany</td><td></td></tr><tr><td><strong>2nd Alternative delivery address:</strong></td><td></td><td></td><td></td></tr><tr><td>C. de Embajadores, 147,<br>28045 Madrid,<br>Spain</td><td></td><td></td><td></td></tr></tbody></table>

#### User/Purchaser

<table data-header-hidden><thead><tr><th width="150"></th><th></th><th width="202"></th><th width="211"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Name:</strong></td><td>Henk Becker</td><td>Mareike Schmidt</td><td>Klaus Herpich</td><td>Martin Müller</td><td></td></tr><tr><td><strong>Position:</strong></td><td>CEO</td><td>Purchasing</td><td>Accounting</td><td>Installer</td><td></td></tr><tr><td><strong>User:</strong></td><td>henk.becker@ektek.com</td><td>m.schmidt@ektek.com</td><td>k.herpich@ektek.com</td><td>m.mueller@ektek.com</td><td></td></tr><tr><td><strong>Password:</strong></td><td>b2bsellers</td><td>b2bsellers</td><td>b2b2sellers</td><td>b2bsellers</td><td></td></tr><tr><td><strong>Rights:</strong></td><td>Admin</td><td>Purchasing</td><td>Accounting</td><td>Installer</td><td></td></tr><tr><td><strong>Access to:</strong></td><td>Ektek GmbH, <br>Ektek Spare-Parts GmbH, <br>Ektek Training Center GmbH, <br>Ektek Hausgeräte GmbH</td><td>Ektek Spare-Parts GmbH, <br>Ektek Hausgeräte GmbH</td><td>Ektek Spare-Parts GmbH, <br>Ektek Training Center GmbH, <br>Ektek Hausgeräte GmbH</td><td>Ektek Spare-Parts GmbH, </td><td></td></tr><tr><td></td><td><a href="https://luxon.demo.b2b-sellers.com/login/email/henk.becker@ektek.com/hash/mitarbeiter"><mark style="color:blue;">Jetzt testen ></mark></a></td><td><a href="https://luxon.demo.b2b-sellers.com/login/email/m.schmidt@ektek.com/hash/mitarbeiter"><mark style="color:blue;">Jetzt testen ></mark></a></td><td><a href="https://luxon.demo.b2b-sellers.com/login/email/k.herpich@ektek.com/hash/mitarbeiter"><mark style="color:blue;">Jetzt testen ></mark></a></td><td><a href="https://luxon.demo.b2b-sellers.com/login/email/m.mueller@ektek.com/hash/mitarbeiter">Jetzt testen ></a></td><td></td></tr></tbody></table>

### Further test customers

#### private customer:

<table data-header-hidden><thead><tr><th></th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>No B2B platform access</td><td></td><td></td></tr><tr><td>Name: Celina Wagner</td><td></td><td></td></tr><tr><td>User: c.wagner@web.de</td><td></td><td></td></tr><tr><td>Password: b2bsellers</td><td></td><td></td></tr><tr><td><a href="https://luxon.demo.b2b-sellers.com/account/login"><mark style="color:blue;">Jetzt testen ></mark></a></td><td></td><td></td></tr></tbody></table>

#### B2B platform customer with one employee

AllInOne Stahlhandel AG\
**info@allinone-stahl.de**\
Hauptstr. 1,\
65663 Hintertupfingen

<table><thead><tr><th>User/Purchaser:</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>Name: Max Wagner</td><td></td><td></td></tr><tr><td>User: ma.wagner@allinone-stahl.de</td><td></td><td></td></tr><tr><td>Password: b2b2sellers</td><td></td><td></td></tr><tr><td><a href="https://luxon.demo.b2b-sellers.com/account/login"><mark style="color:blue;">Jetzt testen ></mark></a></td><td></td><td></td></tr></tbody></table>

#### B2B platform customer with one employee

Max Mustermann GmbH\
**info@mustermann.de**\
Nebenstr. 1,\
65663 Hintertupfingen

<table><thead><tr><th>User/Purchaser</th><th data-hidden></th><th data-hidden></th></tr></thead><tbody><tr><td>Name: Anna Meister</td><td></td><td></td></tr><tr><td>User: a.meister@mustermann.de</td><td></td><td></td></tr><tr><td>Password: b2bsellers</td><td></td><td></td></tr><tr><td><a href="https://luxon.demo.b2b-sellers.com/account/login">J<mark style="color:blue;">etzt testen ></mark></a></td><td></td><td></td></tr></tbody></table>

How to create test-customer, please take a look into our "[`Install and Configuration Guide Video`](https://www.youtube.com/watch?v=R\_d9gIZ0\_q4)"
