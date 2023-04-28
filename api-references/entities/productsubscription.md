# ProductSubscription

Table-name: b2b\_product\_subscription

#### Plugin

{% content-ref url="../../user-guide/configuration-of-purchasable-addons/subscription-article.md" %}
[subscription-article.md](../../user-guide/configuration-of-purchasable-addons/subscription-article.md)
{% endcontent-ref %}

### Table columns

| Field             | Class                | Type     | Is required |
| ----------------- | -------------------- | -------- | ----------- |
| id                | IdField              | binary   | true        |
| customerId        | FkField              | binary   | true        |
| productId         | FkField              | binary   | true        |
| currencyId        | FkField              | binary   | true        |
| billingAddressId  | FkField              | binary   | false       |
| shippingAddressId | FkField              | binary   | false       |
| shippingMethodId  | FkField              | binary   | false       |
| paymentMethodId   | FkField              | binary   | false       |
| salesChannelId    | FkField              | binary   | true        |
| quantity          | IntField             | int      | true        |
| interval          | StringField          | varchar  | true        |
| unitPrice         | FloatField           | double   | false       |
| totalPrice        | FloatField           | double   | false       |
| type              | StringField          | varchar  | false       |
| price             | CalulatedPriceField  | json     | true        |
| priceDefinition   | PriceDefinitionField | json     | false       |
| canceled          | BoolField            | tinyint  | false       |
| lastOrderDate     | DateField            | Datetime | false       |
| nextOrderDate     | DateField            | Datetime | false       |
| customFields      | CustomFields         | json     | false       |
| updateAt          | UpdateAtField        | Datetime | false       |
| createdAt         | CreatedAtField       | Datetime | true        |

### Associations

| Field           | Entity                    | Class                     |
| --------------- | ------------------------- | ------------------------- |
| product         | SalesChannelProductEntity | ManyToOneAssociationField |
| customer        | CustomerEntity            | ManyToOneAssociationField |
| currency        | CurrencyEntity            | ManyToOneAssociationField |
| bilingAddress   | CustomerAddressEntity     | ManyToOneAssociationField |
| shippingAddress | CustomerAddressEntity     | ManyToOneAssociationField |
| shippingMethod  | ShippingMethodEntity      | ManyToOneAssociationField |
| paymentMethod   | PaymentMethodEntity       | ManyToOneAssociationField |
| orders          | OrderEntity               | ManyToOneAssociationField |
