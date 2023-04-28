# CustomerActivityType

Table-name: b2b\_customer\_activity

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/b2boffers.md" %}
[b2boffers.md](../../../user-guide/configuration-of-purchasable-addons/b2boffers.md)
{% endcontent-ref %}

### Table columns

| Field     | Class          | Type     | Is required |
| --------- | -------------- | -------- | ----------- |
| id        | IdField        | binary   | true        |
| label     | StringField    | varchar  | false       |
| name      | StringField    | varchar  | false       |
| iconName  | StringField    | varchar  | false       |
| updatedAt | UpdatedAtField | Datetime | false       |
| createdAt | CreatedAtField | Datetime | true        |
