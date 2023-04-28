# CustomerPrice

Table-name: b2b\_customer\_price

#### Plugin

{% content-ref url="../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Table columns

| Field            | Class                 | Type     | Is required |
| ---------------- | --------------------- | -------- | ----------- |
| id               | IdField               | binary   | true        |
| customerId       | FkField               | binary   | true        |
| productId        | FkField               | binary   | true        |
| productVersionId | ReferenceVersionField | binary   | true        |
| currencyId       | FkField               | binary   | false       |
| prductnumber     | StringField           | varchar  | false       |
| currencyIsoCode  | StringField           | varchar  | false       |
| customerNumber   | StringField           | varchar  | false       |
| from             | FloatField            | Float    | false       |
| to               | FloatField            | Float    | false       |
| priceNet         | FloatField            | Float    | false       |
| pseudoPriceNet   | FloatField            | Float    | false       |
| updatedAt        | UpdatedAtField        | Datetime | false       |
| createdAt        | CreatedAtField        | Datetime | true        |

### Associations

| Field    | Entity         | Class                     |
| -------- | -------------- | ------------------------- |
| customer | CustomerEntity | ManyToOneAssociationField |
| product  | ProductEntity  | ManyToOneAssociationField |
| currency | CurrencyEntity | ManyToOneAssociationField |
