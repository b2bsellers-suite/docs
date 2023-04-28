# B2bProductList

Table-name: b2b\_product\_list

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/order-lists.md" %}
[order-lists.md](../../../user-guide/configuration-of-purchasable-addons/order-lists.md)
{% endcontent-ref %}

### Tabellen Spalten

| Field          | Class          | Type     | Is required |
| -------------- | -------------- | -------- | ----------- |
| id             | IdField        | binary   | true        |
| name           | StringField    | varchar  | false       |
| sessionId      | StringField    | varchar  | false       |
| customerId     | FkField        | binary   | true        |
| employeeId     | FkField        | binary   | false       |
| listTypeId     | FkField        | binary   | true        |
| salesChannelId | FkField        | binary   | true        |
| customFields   | CustomFields   | json     | false       |
| updatedAt      | UpdatedAtField | Datetime | false       |
| createdAt      | CreatedAtField | Datetime | true        |

### Associations

| Field        | Entity                   |                           |
| ------------ | ------------------------ | ------------------------- |
| customer     | CustomerEntity           | OneToOneAssociationField  |
| listType     | SalesChannelEntity       | OneToOneAssociationField  |
| salesChannel | SalesChannelEntity       | OneToOneAssociationField  |
| items        | B2bProductListItemEntity | OneToManyAssociationField |
| employee     | EmployeeEntity           | OneToOneAssociationField  |
