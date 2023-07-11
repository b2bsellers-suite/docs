# OfferAddress

Table-name: b2b\_offer\_address

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/b2boffers.md" %}
[b2boffers.md](../../../user-guide/configuration-of-purchasable-addons/b2boffers.md)
{% endcontent-ref %}

### Table Columns

| Field                  | Class          | Type     | Is required |
| ---------------------- | -------------- | -------- | ----------- |
| id                     | IdField        | binary   | true        |
| countryId              | FkField        | binary   | true        |
| countryStateId         | FkField        | binary   | false       |
| salutationId           | FkField        | binary   | false       |
| firstName              | StringField    | varchar  | false       |
| lastName               | StringField    | varchar  | false       |
| street                 | StringField    | varchar  | true        |
| city                   | StringField    | varchar  | true        |
| company                | StringField    | varchar  | false       |
| department             | StringField    | varchar  | false       |
| title                  | StringField    | varchar  | false       |
| vatId                  | StringField    | varchar  | false       |
| phoneNumber            | StringField    | varchar  | false       |
| additionalAddressLine1 | StringField    | varchar  | false       |
| additionalAddressLine2 | StringField    | varchar  | false       |
| updatedAt              | updatedAtField | Datetime | false       |
| createdAt              | CreatedAtField | Datetime | true        |

### Associations

<table><thead><tr><th>Field</th><th width="237.33333333333331">Entity</th><th>Class</th></tr></thead><tbody><tr><td>country</td><td>CountryEntity</td><td>ManyToOneAssociationsField</td></tr><tr><td>countryState</td><td>CountryStateEntity</td><td>ManyToOneAssociationsField</td></tr><tr><td>orderDeliveries</td><td>OrderDeliveryEntity</td><td>OneToManyAssociationsField</td></tr><tr><td>salutation</td><td>SalutationEntity</td><td>ManyToOneAssociationsField</td></tr></tbody></table>
