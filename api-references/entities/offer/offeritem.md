# OfferItem

Table-name: b2b\_offer\_item

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/b2boffers.md" %}
[b2boffers.md](../../../user-guide/configuration-of-purchasable-addons/b2boffers.md)
{% endcontent-ref %}

### Table columns

| Field           | Class                | Type     | Is required |
| --------------- | -------------------- | -------- | ----------- |
| id              | IdField              | binary   | true        |
| offerId         | FkField              | binary   | true        |
| productid       | FkField              | binary   | false       |
| label           | StringField          | varchar  | false       |
| description     | StringField          | varchar  | false       |
| quantity        | FloatField           | double   | false       |
| unitPrice       | FloatField           | double   | false       |
| totalPrice      | FloatField           | double   | false       |
| price           | CalulatedPriceField  | json     | false       |
| payload         | JsonField            | json     | false       |
| priceDefinition | PriceDefinitionField | json     | false       |
| type            | StringField          | varchar  | true        |
| stackable       | BoolField            | tinyint  | false       |
| removeable      | BoolField            | tinyint  | false       |
| good            | BoolField            | tinyint  | false       |
| optional        | BoolField            | tinyint  | false       |
| position        | Intfield             | int      | false       |
| discount        | FloatField           | double   | false       |
| comment         | LongTextField        | text     | false       |
| customFields    | CustomFields         | json     | false       |
| updatedAt       | UpdatedAtField       | Datetime | false       |
| createdAt       | CreatedAtField       | Datetime | true        |

### Associations

| Field   | Entity                    | Class                     |
| ------- | ------------------------- | ------------------------- |
| product | SalesChannelProductEntity | OneToOneAssociationField  |
| offer   | OfferEntity               | ManyToOneAssociationField |
