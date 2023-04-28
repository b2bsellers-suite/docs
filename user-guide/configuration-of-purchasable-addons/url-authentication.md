---
description: 'Login via URL Hash | Technical Pluginname: B2bUrlAuthentication'
---

# URL Authentication

With the help of the URL authentication plugin there is a simplified possibility for the different user groups to login.

## **Functionality**

The store URL is extended by the user's e-mail address and an individual hash.

The hash is stored in the backend for the user groups customers, buyers and sales staff. The overall URL can be copied from the B2B platform's account management and saved for example in the browser's favorites.

### Structure of the URL

![](<../../.gitbook/assets/01 URL Authentication.png>)

### Enable URL authentication

1. Navigate to the Account tab in the B2B platform.
2. Activate the slide bar "Yes, I want a custom login link".

### **Do you want URL authentication also for sales employees or for private customers?**

You can store the hash for the entity "employee" and "customer". This also means that you can store a hash for sales employees or private customers in the Shopware Administration and they can then also log in via link.

Navigate in the Shopware Administration to "Customers > Overview".

1. Click on "Edit" to be able to edit the corresponding user.
2. Scroll down the "General" tab to "Custom fields".
3. Enter the "Hash for URL authentication" and click on "Save".

![](<../../.gitbook/assets/02 Add B2B Auth Hash to an Employee.png>)

{% hint style="info" %}
Note Alert: Please enter a secure hash of at least 25 characters. \
Please do not use umlauts.
{% endhint %}
