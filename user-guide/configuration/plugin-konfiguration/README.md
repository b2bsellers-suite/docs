---
description: Necessary configuration for the plugin
---

# Configuration of the CORE

{% embed url="https://www.youtube.com/watch?v=R_d9gIZ0_q4" %}

To use the CORE plug-in, the following settings are necessary:

{% hint style="info" %}
Extensions > My Extensions > B2bSellersCore > Configuration
{% endhint %}

## Admin-API

The Admin API requires a user name and password as login data.&#x20;

For the respective "Store API", the access key must be stored, which can be found in the store front.&#x20;

## General Shop Settings

The general store settings are used to set the privacy of the store. The store operator can decide whether and which pages should be made available to the user only with login.

### "Shop access only possible when logged in".

When activated, the user can only access the login area. The rest of the store is locked. Typical use cases are spare parts stores or closed stores, where only customers with access data are allowed to access the shop.

### "Show navigation only when logged in".

If activated, the category navigation will only be displayed for logged-in users.

### "Pages visible before login"

Enter here pages which should be visible for the user without login.

![](<../../../.gitbook/assets/01 General Shop Settings.png>)

## **Documents archive**

The document archive is displayed in the store operator's portal via the "Documents" tab. Here, for example, invoices can be archived.

"Relative path from server root"

Enter the path to the store's document archive.

The server root is the first folder of the server.

**Note**: Make sure that the server root is outside the "www". If the path is available via "https://", protected data can be accessed. This should be avoided under all circumstances!!!!!

### "Structure of file names"

Define the structure of the documents that will be archived.

You can find the possible text modules under the blue question mark in the upper right corner of the text field:

Available variables: {customerNumber}, {type}, {year} and {documentNumber}. Use \* as a wildcard.

![](<../../../.gitbook/assets/02 Document archive.png>)

## **Products**

In the product settings, access rights to product information and the shopping cart are set.

### "Hidden product prices when not logged in".

When activated, product prices are displayed only for logged-in users.

### "Add items to cart only possible in logged-in state".

When activated, items can be added to the shopping cart only by logged-in users.

### "Show change between grid and list view in listing".

When activated, a button is displayed in the product view for logged-in users.

This button is used to switch between grid and table view.

{% hint style="info" %}
_Note: In the table view, a default set of loaded variants is stored. Further variants can be displayed by clicking on the "Load more" button._ Extensions > My Extensions > B2bSellersCore > Configuration
{% endhint %}

How to add more properties in the table view by the store owner, you can find in the Video "how to extend the b2b platform"

![](<../../../.gitbook/assets/03 Products.png>)

## **Order history**

The following settings can be used to provide additional ordering functionality to the user.

### **"Output note field".**

When activated, the "Notes" field is made available. This field will be displayed in the last order step and the text stored there applies to the entire order. The `"b2b_order_customer_note"` custom field on the order can be used normally.

{% hint style="info" %}
You can find the setting for comment fields per order position under Categories > Products > The desired product > B2B Specifications > B2B Product > Show comment
{% endhint %}

### **"Show commission field "**

When activated, the "Commission text" field is made available. This field will be displayed at the last order step and the text stored there will be valid for the entire order. Custom field on the order: b2b\_order\_customer\_commission

### **"Show empty shopping cart"**

When enabled, the "Empty shopping cart" button is made available in the shopping cart.

### &#x20;**"Enable order confirmation mail recipient selection".**

Allows selection of email recipients on the checkout page.

### &#x20;**"Email dispatch recipients of the order confirmation".**

Enter the desired recipients of the order confirmation. The default value of Shopware is the email address of the customer. For each order (in the storefront checkout) you can also set who should receive the order confirmation.

### &#x20;**"Show Express Checkout"**

When activated, the "Express Checkout" button is made available in the off-canvas menu of the shopping cart and in the shopping cart itself. This button will display a popup that allows you to immediately trigger a payable order with the payment method you have stored.

### **"Default payment method for Quick-Checkout".**

Set the payment method that should be made available to the user during the quick checkout, if no personal default payment method is set in the express checkout settings.

### &#x20;**"Activate permanent shopping cart"**

Shopware standard has only a browser session-based shopping cart. Even if you log in this is session based. In the B2Bsellers Suite, the store operator can choose whether the shopping cart can be used "company-wide" by default for all customers, or whether the shopping cart is different "per company and employee", or "whether it is different per employee", but in the latter case, the shopping cart will be recalculated for each customer change, because each customer can be assigned different product prices and customer groups.

The summarized advantage is that any setting of the shopping cart is bound to the customer or employee and is therefore also available on any device.

### &#x20;**"Consumer view without price display"**

When activated, all prices are simply hidden in the storefront. You can use this function e.g. to show the products to an end customer, but no prices.

![](<../../../.gitbook/assets/04 Checkout.png>)

## **Registration process**

The registration process is customized by the following settings:

### **"Create the first admin employee when creating a customer".**

When activated, by creating a customer, the first stored employee will be set as admin. This means every newly registered customer will be automatically created as an "Employee" as well.

### &#x20;**"Send welcome mail if flag exists"**

When activated, the customer will receive a welcome mail as soon as he has been created by the store operator and the parameter "sendWelcomeMail" has been stored in the request.

### &#x20;**"Send welcome mail when customer is created"**

When activated, the customer will receive a welcome mail as soon as he has been created by the store operator.

### &#x20;**"Registration request form instead of registration".**

When activated, an inquiry form is displayed in the storefront instead of an actual registration form. Direct registration of the customer in the store is not possible. The store operator must register the customer in the system. This setting is recommended for store operators who create all customers in the merchandise management system first and then transfer them from there to the store system. The registration request will be sent simply by e-mail to the store operator's e-mail address.

### &#x20;**"Business confirmation in the registration".**

When activated, there will be a possibility to upload a business confirmation in the registration process. This setting is only possible if the request form is available. It is not possible in case of actual registration, because we do not save the business confirmation in the customer account.

### &#x20;**"Customers are registered as B2b customers".**

When activated, the "Business Customer" selection field is made available to the customer in the registration process. This gives him access to the B2B area of the store.

![](<../../../.gitbook/assets/05 Registration process.png>)

## **Platform**

The platform settings are used by the store operator to customize its display.

### &#x20;**"Customer Navigation"**

The entry point of the B2B navigation should be stored here. This will then be used for the B2B platform navigation as a logged-in "employee". The navigation can be edited under "Extensions> B2B-platform menu".

### &#x20;**"Sales Agent Navigation"**

The entry point of the sales platform navigation should be stored here. This will then be used for the sales platform navigation as a logged-in "sales agent". The navigation can be edited under "Extensions> B2B-platform menu".

### &#x20;**"Issue orders to all assigned customers "**

When activated, the orders of all assigned customers are displayed to the store operator.

When deactivated, only the orders of the currently logged-in customers.

### &#x20;**"Demo installation"**

When activated, the "Send Feedback" marker is displayed at the top of the screen in the demo installation.

Note: In live mode, this feature should be disabled.

### &#x20;**"Cockpit Widgets in Dashboard".**

Select whether and if yes, where in the dashboard should the cockpit widgets be displayed.

### &#x20;**"Target page after login"**

Select which page should be displayed first after a login. However, each employee can also overwrite this in his profile.

![](<../../../.gitbook/assets/06 Platform.png>)

## **Worlds of Experience**

The B2Bsellers suite offers the store operator experience worlds, which can be preconfigured for the employees. The experience worlds are selected in the following settings.

![](<../../../.gitbook/assets/07 Shopping Experiences.png>)

### &#x20;**"Employee dashboard experience world"**

Select the experience world which should be displayed to the store employees on their dashboard.

### &#x20;**"Sales dashboard experience world"**

Select the experience world which should be displayed to sales employees on their dashboard.

### **Fallback contact person**

&#x20;If a customer has not yet been assigned a contact person, a fallback contact person will be displayed. This can be stored here:

![](<../../../.gitbook/assets/08 Fallback Contact Person.png>)

### &#x20;**Passwordless Login**

Here you can set how long the link is valid after sending the mail.

![](<../../../.gitbook/assets/09 Passwordless Login.png>)

### &#x20;**Customer activities**

Here you can decide whether the customer activities of "B2B Platform" customers will be tracked and clearly displayed to the sales employee in the sales platform.

![](<../../../.gitbook/assets/10 Customer Activity.png>)

