# Easy activate all Addons and Features

As you know, the B2Bsellers Suite uses Symfony bundles to divide individual functions into components that can be activated individually.

When you reinstall the B2B Suite, no addons/features are activated from the start. However, if you would like to have everything activated, you can simply copy the following content into the **/var/b2b-license.json** file, then all features and addons are activated.



{% hint style="info" %}
Please keep in mind that you always have to rebuild the admin, the storefront and the B2B platform when activating addons.
{% endhint %}

```
// var/b2b-license.json

{
  "restrictions": {
    "salesRepresentativeLimit": 5,
    "employeeLimit": 3
  },
  "addons": {
    "0": "B2bOffer",
    "1": "B2bEmployeeBudgets",
    "3": "B2bProductSubscription",
    "4": "B2bEventArticle",
    "7": "B2bSalesRepresentativeFastOrder",
    "8": "B2bCopperBrassSurcharge",
    "9": "B2bSpareParts",
    "10": "B2bDiscountRate",
    "11": "B2bCostCenter",
    "12": "B2bPartialAssortments",
    "13": "B2bMobileSalesPortalApp",
    "14": "B2bEventManager"
  },
  "features": [
    "B2bBonusProgram",
    "B2bProductRequest",
    "B2bUrlAuthentication",
    "B2bPdpVariantList",
    "B2bProductLists"
  ]
}
```

## Necessary builds after activation of addons

Please run the following build processes in your console:

```
bin/console b2b:platform:build
bash ./bin/build-storefront.sh
bash ./bin/build-administration.sh
```

