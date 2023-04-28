# ProductSubscriptionOrder

Table-name: b2b\_product\_subscription\_order

#### Plugin

{% content-ref url="../../user-guide/configuration-of-purchasable-addons/subscription-article.md" %}
[subscription-article.md](../../user-guide/configuration-of-purchasable-addons/subscription-article.md)
{% endcontent-ref %}

### Table columns

| Field                    | Class   | Type   | Is required |
| ------------------------ | ------- | ------ | ----------- |
| b2bProductSubscriptionId | FkField | binary | true        |
| orderId                  | FkField | binary | true        |

### Associations

| Field                  | Entity                    | Class                     |
| ---------------------- | ------------------------- | ------------------------- |
| b2bProductSubscription | ProductSubscriptionEntity | ManyToOneAssociationField |
| order                  | OrderEntity               | ManyToOneAssociationField |
