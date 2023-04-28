# UseCustomer URL Parameter

## **What is the "useCustomer" URL parameter?**

The "useCustomer" URL parameter can be used when linking a B2bPlatform URL if you want to tell in a link that a specific customer should be used for the target page.

A company user can buy for several companies. However, when e.g. an offer or an order is triggered, the user indeed orders for a specific customer.  But if the customer is currently logged in for another customer and clicks on a link in the email, the target page "correctly" cannot be opened. However, if the "useCustomer" parameter is handed over, the user will be logged in accordingly for the correct customer before calling up the URL, provided this customer is assigned to him.

#### **Notes**

* This URL parameter can currently only be used in the controller: /b2b\_platform (i.e. all Vue.Js B2BPlatform URLs).
* You can use either the customer number or the customer ID as parameter

#### **Example:**

Currently, this "useCustomer" function will be used in the "Offer function" to send the offer to the end customer. If the customer then clicks on the "Order offer" button, he will be logged directly into the correct customer and can order the offer in the pop-up.

**Recommendation:**

Please use the "useCustomer" parameter when developing individual functions when sending mail or generating URLs that can then be sent to third parties. For security purposes, the customer number should be used and not the customer UUID.
