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

| Field           | Entity              | Class                      |
| --------------- | ------------------- | -------------------------- |
| country         | CountryEntity       | ManyToOneAssociationsField |
| countryState    | CountryStateEntity  | ManyToOneAssociationsField |
| orderDeliveries | OrderDeliveryEntity | OneToManyAssociationsField |
| salutation      | SalutationEntity    | ManyToOneAssociationsField |
