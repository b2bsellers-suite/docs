# How to add „Menü Item“ on B2BPlattform

In the B2B platform (whether for buying customers or for sales representatives) there is a separate navigation. This navigation can be maintained in the Shopware admin area and individual menu items can be created from the respective plugins.

We recommend creating the menu items directly in the setup script for each custom plugin so that the menu items are immediately visible after installation.

## Features:

* The menu items are a separate entity ("XXXXX").
* It can be set in the plug-in config which entry points the sales representative and the buyer have. This way, 2 navigation trees can be set up (Thus you could also build a separate navigation structure for each sales channel/language).
* Multilingualism is of course possible
* The menu items can also be entered manually in the Shopware Admin. Via the plug-in script, an additional flag can be set: "is deletable". This means that the menu item comes from a plug-in and therefore may not be deleted. It can of course be deactivated or deleted via the database. However, the menu ID is usually necessary for certain queries. Deleting via the database is only recommended for developers who know what they are doing.
* Via "Shopware Rules" menu items can also be hidden/shown.
* An icon/image can be inserted in front of the menu item
* You can set the target individually
  * &#x20;B2Bplatform link (with vue-router) or
  * Category Link with entity-connection
  * External Link (https://www. \* )
  * nternal Shop-Link (link without https and domain)

## **Automatic creation of menu items in a plug-in setup script:**

Add a script in your setup script or migration accordingly to automatically create menu items on installation.

#### Example:

![](<../../.gitbook/assets/image (19).png>)

## **Creation of menu items in the Admin (manually)**

1. Click on Extensions -> B2B-Platform menu

![](<../../.gitbook/assets/image (12).png>)

2\. You can now sort and edit the menu items like the Shopware standard categories.

![](<../../.gitbook/assets/image (2).png>)

3\. On this screenshot, the "internal link" is still missing.

![](<../../.gitbook/assets/image (22).png>)

4\. You can add Shopware icons or images from the media library.



![](<../../.gitbook/assets/image (13).png>)



![](<../../.gitbook/assets/image (17).png>)

## Setting the entry points in the B2Bsellers Core Plugin settings:

![](<../../.gitbook/assets/image (16).png>)
