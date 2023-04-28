---
description: Installing the B2B Platform
---

# Installation

{% embed url="https://www.youtube.com/watch?v=R_d9gIZ0_q4" %}

## Install

1. Upload files to custom/plugins/b2bsellerscore
2. install and activate the Plugin at the Shopware Backend
3. Or run in console `bin/console plugin:refresh && bin/console plugin:install b2bsellerscore && bin/console plugin:activate b2bsellerscore`&#x20;
4. go to console and run command `bin/console b2b:platform:build` at root directory
5. run `bin/console cache:clear`

\=> if you want: run `bin/console b2b:create:test-data` for insert default test data (customer/contacts) li

{% content-ref url="test-daten.md" %}
[test-daten.md](test-daten.md)
{% endcontent-ref %}

Info: we recommend the install over the cli, not over the shopware backend - sometimes there are errors

first, you have to install the "B2Bsellers Core" Plugin.

### Install-Script for all B2Bsellers Suite Plugins&#x20;

We recommend to use our script to install all B2Bsellers Plugins within one command. You can change all used plugins...

```
#!/bin/bash

echo "Installing all B2bSellers Suite Plugins"

bin/console plugin:refresh
bin/console plugin:install -ac B2bSellersCore

bin/console plugin:install -ac B2bPlatformTheme B2bProductLists B2bProductRequest B2bOffer B2bEmployeeBudgets B2bBonusProgram B2bBlocksCollection B2bEventArticle B2bSpareParts B2bCostCenter B2bCopperBrassSurcharge B2bUrlAuthentication B2bproductSubscription B2bPdpVariantList B2bRegisterRequest

bin/console theme:change b2bplatformtheme
bin/console b2b:platform:build

bash ./bin/build-storefront.sh
bash ./bin/build-administration.sh

exit 0
```

## Important: With every activation/deactivation of the addons the Javascript and the CSS must be built afterwards.

Because all addons are "Symfony bundles", it is necessary to execute the following commands after each addon activation/deactivation:

* bin/console b2b:platform:build
* bash bin/build-administration.sh
* bash bin/build-storefront.sh

## Setup

1. Change the plugin configuration (admin api and store api credentials are needed)
2. Add emails to the following "business events": account\_activation.send and account\_request.send

## Api

Flag for sending welcome mail via api (customer create + update) -> \_sendWelcomeMail

## Console commands

#### 5.1 Entity Mapping Command (CustomerPrices):

**Usage:**

`bin/console b2b:entity:map`

#### 5.2 Platform watch command

**Usage:**

`bin/console b2b:platform:watch <user> <password>`

**Arguments:**

| Argument     | Description                |
| ------------ | -------------------------- |
| **user**     | Customer/Employee E-Mail   |
| **password** | Customer/Employee password |

**Example:**

Sales Agent: `bin/console b2b:platform:watch m.sommer@luxon.de mediagraphik` Customer-Employee `bin/console b2b:platform:watch Henk.Becker@bosch-pt.com mediagraphik`

