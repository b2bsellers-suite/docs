# EmployeeRole

Table-name: b2b\_employee\_role

#### Plugin

{% content-ref url="../../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Tabellen Spalten

| Field      | Class           | Type     | Is required |
| ---------- | --------------- | -------- | ----------- |
| id         | IdField         | binary   | true        |
| name       | TranslatedField | varchar  | false       |
| customerId | FkField         | binary   | false       |
| privileges | Listfield       | json     | true        |
| updatedAt  | UpdatedAtField  | Datetime | false       |
| createdAt  | CreatedAtField  | Datetime | false       |

### Associations

| Field             | Entity                 | Class                        |
| ----------------- | ---------------------- | ---------------------------- |
| employeeCustomers | EmployeeCustomerEntity | OneToManyAssociationField    |
| customer          | CustomerEntity         | ManyToOneAssociationField    |
| name              | ToDo                   | TranslationsAssociationField |

### EmployeeRoleTranslation

| Field | Class       | Type    | is required |
| ----- | ----------- | ------- | ----------- |
| name  | StringField | varchar | true        |
