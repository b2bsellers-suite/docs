# SalesRepresentativeCustomer

Table-name: b2b\_sales\_representative\_customer

#### Plugin

{% content-ref url="../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Table columns

| Field      | Class          | Type     | Is required |
| ---------- | -------------- | -------- | ----------- |
| id         | IdField        | binary   | true        |
| salseRepId | FkField        | binary   | true        |
| customerId | FkField        | binary   | true        |
| updatedAt  | UpdatedAtField | Datetime | false       |
| createdAt  | CreatedAtField | Datetime | true        |

### Associations

| Field    | Entity         | Class                     |
| -------- | -------------- | ------------------------- |
| customer | CustomerEntity | ManyToOneAssociationField |
