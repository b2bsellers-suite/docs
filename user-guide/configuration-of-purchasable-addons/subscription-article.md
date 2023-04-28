---
description: 'Directory: custom/plugins/B2BSellersCore/addons/B2bProductSubscription'
---

# Subscription Article

With the B2Bsellers product subscriptions plugin, the shop operator has the option of offering his customers interval deliveries in the form of subscriptions. For this purpose, the shop operator decides which products are eligible for subscription and which discount should be granted for a subscription.

Costumers and buyers have thereby the advantage of being able to trigger recurring orders automatically.

## **Features**

*   Individual products can be configured to subscription products by the shop operator.

    Custom field on product: b2b\_subscription\_enabled
* Each subscription product can be given its own discount value to convince the buyer to order a subscription.
* Subscriptions can be managed by the buyer in the B2B platform
  * View all subscriptions
  * Change delivery intervals
  * Delete subscription
* Subscribed products can only be paid with the payment methods "invoice" and "prepayment" (third-party providers such as PayPal are not supported).

## **Planned features**

* Subscriptions cannot later be changed by customers/purchasers, but must be terminated. Considering the termination period, etc.
*   Show subscription products exclusively as interval products.

    Thus, it can be decided separately for each product whether a one-time delivery can be accepted at all.
* Display of subscriptions in the Shopware admin area

On the current roadmap**,** it is not planned to allow subscription orders via payment service providers like PayPal. If you wish to do so, please contact us.

## **Enable subscription per product**

1. Navigate to "Catalogues" -->"Products" in the administration and open the product you want to enable as a subscription product.
2. Navigate to the Specifications tab
3. Scroll down to the menu item "Additional fields".
4. Activate "Allow subscription option".
5. Enter the discount (in percent) which the customer should receive through this subscription.

![Activate subscription per product](<../../.gitbook/assets/Activate subscription per product.png>)

## **Functions/extensions in the frontend**

### _In the product overview_

By activating the subscription function, customers/buyers have the option of selecting a subscription in addition to the one-off delivery.

The associated savings through a discount are displayed next to the selection button. If customers/buyers choose the subscription, they will be given a further selection option to set the delivery interval.

![Extensions in the frontend - product overview](<../../.gitbook/assets/Extensions in the frontend - product overview.png>)

### _In the shopping cart_

Products for which a subscription has been taken out are marked with a subscription badge in the shopping cart. Hence, it is for costumers/buyers directly recognizable that it is a subscription product.

![Extensions in the frontend - Shopping Cart](<../../.gitbook/assets/Extensions in the frontend - Shopping Cart.png>)

### Subscription management in the B2B platform

Under "My products" is provided the menu item "Subscriptions".

Here customers/buyers can view their completed subscriptions and the following details:

* Article name
* Current unit price (the original price is displayed next to it)
* Quantity (per delivery)
* Created on
* Delivery interval with the option to change it
* Billing address
* Delivery address
* Next delivery

In addition, the subscription can be deleted here.

![Management of the subscription in the B2B platform](<../../.gitbook/assets/Management of the subscription in the B2B platform.png>)

## **Technical information:**

_Data structure:_

<table data-header-hidden><thead><tr><th>Explanation</th><th>Field</th><th data-hidden></th></tr></thead><tbody><tr><td>b2b_subscription_enabled</td><td>Is this product a subscription product?</td><td></td></tr><tr><td>b2b_subscription_discount</td><td>Discount rate if the buyer decides for recurring deliveries.</td><td></td></tr></tbody></table>

Database table in which all subscriptions are stored: b2b\_product\_subscription

Automatic execution of the order

Through a Shell-command 'php bin/console b2b:product-subscription:order' all subscription orders that have to be executed for the executed day will be executed.

A cronjob should be set up that automatically executes this command 1x per day.

## Entities

{% content-ref url="../../api-references/entities/productsubscription.md" %}
[productsubscription.md](../../api-references/entities/productsubscription.md)
{% endcontent-ref %}

{% content-ref url="../../api-references/entities/productsubscriptionorder.md" %}
[productsubscriptionorder.md](../../api-references/entities/productsubscriptionorder.md)
{% endcontent-ref %}
