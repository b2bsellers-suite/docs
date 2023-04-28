# ProductExplodedView

Table-name: b2b\_product\_exploded\_view

#### Plugin

{% content-ref url="../../user-guide/configuration-of-purchasable-addons/spare-parts-shop.md" %}
[spare-parts-shop.md](../../user-guide/configuration-of-purchasable-addons/spare-parts-shop.md)
{% endcontent-ref %}

### Table columns

| Field          | Class          | Type     | Is required |
| -------------- | -------------- | -------- | ----------- |
| id             | IdField        | binary   | true        |
| productMediaId | FkField        | binary   | false       |
| posLeft        | StringField    | varchar  | false       |
| posTop         | StringField    | varchar  | false       |
| productId      | FkField        | binary   | false       |
| name           | StringField    | varchar  | false       |
| amount         | StringField    | varchar  | false       |
| markWidth      | StringField    | varchar  | false       |
| markHeight     | StringField    | varchar  | false       |
| customFields   | CustomFields   | json     | false       |
| updatedAt      | UpdatedAtField | Datetime | false       |
| createdAt      | CreatedAtField | Datetime | true        |

### Associations

| Field        | Entity             | Class                     |
| ------------ | ------------------ | ------------------------- |
| productMedia | ProductMediaEntity | ManyToOneAssociationField |
| product      | ProductEntity      | ManyToOneAssociationField |
