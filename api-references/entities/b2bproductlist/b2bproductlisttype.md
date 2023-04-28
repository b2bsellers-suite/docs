# B2bProductListType

Table-Name: b2b\_product\_list\_type

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/order-lists.md" %}
[order-lists.md](../../../user-guide/configuration-of-purchasable-addons/order-lists.md)
{% endcontent-ref %}

### Tabellen Spalten

| Feld                       | Klasse         | Typ      | required |
| -------------------------- | -------------- | -------- | -------- |
| id                         | IdField        | binary   | true     |
| incrementId                | FkField        | binary   | true     |
| comment                    | FkField        | binary   | true     |
| visibleGast                | StringField    | varchar  | false    |
| visibleCustomer            | StringField    | varchar  | false    |
| visibleSalesRepresentative | StringField    | varchar  | false    |
| customFields               | CustomFields   | json     | false    |
| updatedAt                  | UpdatedAtField | Datetime | false    |
| createdAt                  | CreatedAtField | Datetime | true     |
