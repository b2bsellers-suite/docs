# How to import external orders and offers?

## Easiest way: use the B2Bsellers Admin-API Order creation Endpoint

We know that in B2B platforms "store owners" have the requirement that all orders (whether ERP or external sources) are available in the Shopware shop / E-Commerce Platform. \
Although Shopware is already API-driven and it is possible to create an order via the Shopware Admin API for customers, but it needs deep know-how.

For this reason, we at B2Bsellers have created an **absolutely simple ADMIN-API endpoint for creating orders and offers**, which makes it possible to create an order/offer for customers with some less data. \
\
Advantages of our "simple order creation admin api" are:

* You don't have to use UUIDs, you can also use article numbers, order numbers, customer numbers.
* Specify the product type "custom" and the product does NOT have to exist in shopware.
* Performance: With our API it is possible to create many records at once.

Here you'll find the documentation of the ["Simple order creation" Admin-API Endpoint](../../api-references/admin-api/order-import-endpoint.md)

{% content-ref url="../../api-references/admin-api/order-import-endpoint.md" %}
[order-import-endpoint.md](../../api-references/admin-api/order-import-endpoint.md)
{% endcontent-ref %}

{% hint style="warning" %}
We are working on the easiest way for quote creation via admin-api! Please stay tuned!
{% endhint %}
