# Offer

Table-name: b2b\_offer

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/b2boffers.md" %}
[b2boffers.md](../../../user-guide/configuration-of-purchasable-addons/b2boffers.md)
{% endcontent-ref %}

### Table columns

| Field             | Class                | Type      | Is required |
| ----------------- | -------------------- | --------- | ----------- |
| id                | IdField              | binary    | true        |
| statusId          | FkField              | binary    | true        |
| offerCustomerId   | FkField              | binary    | true        |
| employeeId        | FkField              | binary    | true        |
| number            | StringField          | varchar   | false       |
| deliveryDate      | DateTimeFid          | Datetime  | false       |
| documentDate      | DateTimeField        | Datetime  | false       |
| validUntil        | DateTimeField        | Datetimte | false       |
| matchcode         | StringField          | varchar   | false       |
| commission        | Stringfield          | varchar   | false       |
| process           | StringField          | varchar   | false       |
| editorId          | FkField              | binary    | false       |
| billingAddressId  | FkField              | binary    | true        |
| deliveryAddressId | FkField              | binary    | true        |
| salesChannelId    | FkField              | binary    | true        |
| currencyId        | FkField              | binary    | true        |
| price             | CartPriceField       | json      | false       |
| optionalPrice     | CartPriceField       | json      | false       |
| shippingCosts     | CalculatedPriceField | json      | false       |
| shippingMethodId  | FkField              | binary    | true        |
| deepLinkId        | StringField          | varchar   | false       |
| headerText        | LongTextField        | text      | false       |
| footerText        | LongtextField        | text      | false       |
| file              | StringField          | varchar   | false       |
| customFields      | CustomFields         | json      | false       |
| mailTo            | Stringfield          | varchar   | false       |
| mailCc            | Stringfield          | varchar   | false       |
| updatedAt         | UpdatedAtField       | Datetime  | false       |
| createdAt         | CreatedAtField       | Datetime  | true        |

### Associations

| Field            | Entity                 | Class                     |
| ---------------- | ---------------------- | ------------------------- |
| status           | OfferStatusEntity      | ManyToOneAssociationField |
| offerCustomer    | OfferCustomerEntity    | OneToOneAssociationField  |
| employee         | EmployeeEntity         | ManyToOneAssociationField |
| editor           | CustomerEntity         | ManyToOneAssociationField |
| billingAddress   | OfferAddressEntity     | OneToOneAssociationField  |
| deliveryAddress  | OfferAddressEntity     | OneToOneAssociationField  |
| salesChannel     | SalesChannelEntity     | ManyToOneAssociationField |
| currency         | CurrencyEntity         | ManyToOneAssociationField |
| paymentCondition | PaymentConditionEntity | ManyToOneAssociationField |
| items            | OfferItemEntity        | OneToOneAssociationField  |
| shippingMethod   | ShippingMethodEntity   | ManyToOneAssociationField |
| paymentMethod    | PaymentMethodEntity    | ManyToOneAssociationField |
