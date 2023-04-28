---
description: 'Directory: custom/plugins/B2BSellersCore/addons/B2bCopperBrassSurcharge'
---

# Copper and brass product surcharges

The copper and brass plugin makes it possible to provide products with the current price surcharge for their copper or brass part. Thus, for goods made of copper (e.g. pipes or cables) and brass (e.g. cable glands) price fluctuations can be compensated.

## **Functionality**

In the backend, for individual products, the corresponding share of copper or brass in kilograms is stored via a custom field. The store operator must create a reference article for copper and brass in Shopware. These reference articles represent the current daily exchange price per kilogram and should always be updated. The stored product price is then used as a reference value for 1 KG copper/knife.

The value of goods of the reference articles is multiplied in the B2Bsellers Suite with the stored copper or brass part and added to the article price created in Shopware Standard.

The company employee only sees the final price, not the included surcharge.

## **Plugin configuration**

1. Navigate in the administration to "Extensions"-->"My Extensions" and open the configuration of the plugin "B2Bsellers Suite - Copper & Brass Surcharge".
2. Select the reference articles for the surcharge**:**

![Plugin configuration](<../../.gitbook/assets/01 Settings.png>)

![Amount of copper & brass](<../../.gitbook/assets/02 Amount of copper & brass.png>)

3\. Navigate in the administration to "Catalogs" "Products" and open the product to which the copper and brass price should be added.

4\. Select the "Specifications" tab and scroll to the "Custom fields".

5\. Select the "Copper and brass quantity" tab and enter the quantity of brass and copper that the product contains in the corresponding field.
