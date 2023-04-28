---
description: 'Directory: custom/plugins/B2BSellersCore/addons/B2bSpareParts'
---

# Spare Parts Shop

Compared to their value, spare parts cause a comparatively high consulting expense. The process costs are usually extremely high.

The reason for this is, among other things, the (in)compatibility of spare parts to different models and the related high consulting effort.

With the B2Bsellers Spare Parts Plugin, the online shop becomes a spare parts shop which significantly reduces internal process costs and provides again more free resources for the sales staff.

### **Features**

* Exploded views
* Distinction between spare parts and models
* Search based on
  * model numbers
  * selected properties
* Multi-dimensional accessory groups (cross-selling with individual notes)

### **Planned features**

The device management (in planning) as an additional extension in connection with the spare parts shop will complement each other well, because then the customer can manage all his models/devices in his account and the related spare parts can be used for upselling thanks to the available connections.

## Exploded views

### **Adding exploded views**

1. Navigate in the Shopware administration to "Catalogues" --> "Products" and open there the product to which you would like to add an exploded view.
2. Scroll down to the menu item "Media".
3. Upload the desired exploded view. 4. Click on the advanced button (3 dots) of the graphic preview and select the menu item "is an exploded view".
4. In this way, you can assign several exploded views to one product.
5. The button "exploded view" appears in the Frontend if other gallery media are also displayed on the product detail page.  Otherwise, no buttons are displayed.

![Adding exploded views](<../../.gitbook/assets/Add exploded views.png>)

### **Adding markers to an exploded view**

1. Navigate in the Shopware administration to "Catalogues" --> "Products" and open the product there, to which you want to add an exploded view.
2. Select the tab "Exploded view" in the tabs.
3. You will be displayed the exploded views in the stored order list.
4. Click on the button " Enable marking mode".
5. Click on the desired position in the exploded view.
6. The position is automatically saved and the "Edit marking" menu will open.

![Adding markers to an exploded view](<../../.gitbook/assets/Add marks in an exploded view.png>)

### **Editing markings in an exploded view**

By clicking on a marker, the editing menu opens, in which the following options are available to you.

General:

* Determine the position of the marker (distance to the left and upwards).
* To link the desired product, choose the right product from the drop-down menu from the complete Shopware product range.

Optional fields:

* Enter the desired designation.
* Enter the recommended quantity.
* Change the size of the marker. (Functionless so far, as we currently only illustrate round markers in one size).

Custom Fields:

* Here you can store/create additional fields for the marking.

Click on "Save" to save your settings.

The markings are now displayed on the exploded view in the admin as well as in the Frontend.

The linked products are displayed on mouseover.

The set and recommended quantity is already entered.

The linked products can be placed in the shopping cart directly from the exploded view.

![Editing markings in an exploded view](<../../.gitbook/assets/Edit marks in an exploded drawing.png>)

## **Differentiation between spare parts and models**

With the B2Bsellers Spare Parts Plugin you have the possibility to store products as models. By marking as a model or spare part, a product will be issued correctly in the spare parts search and you can make a differentiation in the Frontend.

The settings for this can be found for the respective product under "Specifications" > "Additional fields".

Note: We are currently planning further features here.

![Distinction between spare parts and models](<../../.gitbook/assets/Distinction between spare parts and models.png>)

## **Search by selected properties**

Shopware Standard makes it possible to store properties for a product (e.g., different colors, sizes, lengths, thread diameters, etc.). The B2Bsellers Spare Parts extension makes it possible for buyers to mark the appropriate properties on the product detail page and by clicking on "Find similar items" to compare products that have exactly the marked properties.

Search for selected properties.

1. In the Frontend of the spare parts shop, the overview of the properties is displayed under the product.
2. Via checkboxes, one or more properties can be selected.
3. Click on the button "Find similar products".
4. The "Comparison of similar products" table opens.

Note: Through the B2Bsellers Core Plugin, properties sets can also be created to bundle multiple properties into one set. This feature is compatible with the sets.

## **Create multi-dimensional accessory groups**

You have the possibility to create multiple accessory groups for one product.

The B2Bsellers Spare Parts Plugin contains an easy-to-understand syntax with which you can maintain the multi-dimensional accessory groups in just one field as an additional field on the product.                                                                  &#x20;

The Shopware standard solution with several cross-selling groups is great, but often ERP systems and interfaces cannot map these groups in the ERP. Our syntax, on the other hand, is a simple additional field on the article, which is also very easy to maintain in an ERP with a standard Shopware 6 interface.&#x20;

We chose the disadvantage of regulating the connection via the product number instead of via a database table and unique identifiers on purpose, because the Shopware solution is good, but not compatible with most ERP solutions.

The great advantage of our syntax is that you can also store additional information such as a note only for a product-to-product connection.

Example: There are many accessories for a machine. A certain part can be used, but another drill hole is necessary. This information can be easily stored in our syntax.

1. Navigate to "Catalogues"--> "Products" -->"B2B Specifications" in the administration.
2. Scroll down to the menu item "Product accessories fields".
3. Activate the checkbox "Show product accessories".
4. In the text area field "Product accessories" you have the following input options with the following syntax, for example, via the syntax linked with the ERP system
   1. Point bracket to the right => Example: "> Heading 1" to create an accessory group.
   2. Enter one or more item numbers to link accessories parts. If this item is not available, it will simply be skipped and not displayed.
   3. "> Heading 2" to create another accessory group.
   4. Add an important note to an article.
   5. Enter behind the article number of the desired product a ";" and complete your individual "Note".
5.  In the Spare Parts shop, the tab "Accessories" will be displayed for the respective product.

    The accessory groups will be displayed below.

#### Syntax example:

```
>Spare parts
7020-01-010
7020-01-009; If used, you must drill an additional Ø6mm hole at the designated mark; Notice in English
4010-02-001
> Tools
18005
18004
18006
>Consumables
50110
50513
>Care and maintenance
50535
50536
50537
```

**Notes:**

* Each line is processed individually. It is important that each article number or heading/group is stored in a line.
* The separation to the note is a semicolon. If there are several languages, you can also work with 2 or more semicolons.
* There is no length limit&#x20;

![](<../../.gitbook/assets/Create multidimensional accessory groups.png>)

**What distinguishes us from Shopware standard cross-selling?**

Many ERP systems cannot fully operate the standard Shopware 6 cross-selling function with several cross-selling groups, as in an ERP system usually only accessories and similar articles can be assigned to an article. Multiple groups are not possible.

Thanks to our syntax, any ERP system can create this additional field and due to the easy-to-learn syntax, also complex accessory groups can be maintained in an ERP system.

In addition, it is possible to include for a specific article connection an individual note.

## Entities

{% content-ref url="../../api-references/entities/productexplodedview.md" %}
[productexplodedview.md](../../api-references/entities/productexplodedview.md)
{% endcontent-ref %}
