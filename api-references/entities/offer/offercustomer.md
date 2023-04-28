# OfferCustomer

Table-name: b2b\_offer\_customer

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/b2boffers.md" %}
[b2boffers.md](../../../user-guide/configuration-of-purchasable-addons/b2boffers.md)
{% endcontent-ref %}

### Table columns

| Field          | Class              | Type     | Is required |
| -------------- | ------------------ | -------- | ----------- |
| id             | IdField            | binary   | true        |
| customerId     | FkField            | binary   | false       |
| email          | StringField        | varchar  | true        |
| salutationId   | FkField            | binary   | false       |
| firstName      | StringField        | varchar  | false       |
| lastName       | StringField        | varchar  | false       |
| company        | StringField        | varchar  | false       |
| title          | StringField        | varchar  | false       |
| customerNumber | StringField        | varchar  | false       |
| customFields   | CustomFields       | json     | false       |
| remoteAddress  | RemoteAddressField | json     | false       |
| updatedAt      | UpdatedAtField     | Datetime | false       |
| createdAt      | CreatedAtField     | Datetime | true        |

### Associations

| Field      | Entity           | Class                     |
| ---------- | ---------------- | ------------------------- |
| customer   | CustomerEntity   | ManyToOneAssociationField |
| salutation | SalutationEntity | ManyToOneAssociationField |
