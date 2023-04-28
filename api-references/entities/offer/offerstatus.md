# OfferStatus

Table-name: b2b\_offer\_status

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/b2boffers.md" %}
[b2boffers.md](../../../user-guide/configuration-of-purchasable-addons/b2boffers.md)
{% endcontent-ref %}

### Table columns

| Field     | Class          | Type     | Is required |
| --------- | -------------- | -------- | ----------- |
| id        | IdField        | binary   | true        |
| label     | StringField    | varchar  | false       |
| confirmed | BoolField      | tinyint  | false       |
| draft     | BoolField      | tinyint  | false       |
| open      | BoolField      | tinyint  | false       |
| declined  | BoolField      | tinyint  | false       |
| updatedAt | UpdatedAtField | Datetime | false       |
| createdAt | CreatedAtField | Datetime | true        |
