# B2bProductListItem

Table-Name: b2b\_product\_list\_item

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/order-lists.md" %}
[order-lists.md](../../../user-guide/configuration-of-purchasable-addons/order-lists.md)
{% endcontent-ref %}

### Table columns

| Feld          | Klasse         | Typ      | required |
| ------------- | -------------- | -------- | -------- |
| id            | IdField        | binary   | true     |
| articleNumber | StringField    | varchar  | false    |
| productId     | FkField        | binary   | true     |
| productListId | FkField        | binary   | true     |
| comment       | StringField    | varchar  | false    |
| position      | StringField    | varchar  | false    |
| quantity      | StringField    | varchar  | false    |
| customFields  | CustomFields   | json     | false    |
| updatedAt     | UpdatedAtField | Datetime | false    |
| createdAt     | CreatedAtField | Datetime | true     |

### Associations

| Field       | Entity                    | Class                    |
| ----------- | ------------------------- | ------------------------ |
| product     | SalesChannelProductEntity | OneToOneAssociationField |
| productList | B2bProductListEntity      | OneToOneAssociationField |
