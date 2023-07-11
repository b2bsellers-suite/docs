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

<table><thead><tr><th width="242">Field</th><th>Entity</th><th width="273.2517985611511">Class</th></tr></thead><tbody><tr><td>employeeCustomers</td><td>EmployeeCustomerEntity</td><td>OneToManyAssociationField</td></tr><tr><td>customer</td><td>CustomerEntity</td><td>ManyToOneAssociationField</td></tr><tr><td>name</td><td>ToDo</td><td>TranslationsAssociationField</td></tr></tbody></table>

### EmployeeRoleTranslation

| Field | Class       | Type    | is required |
| ----- | ----------- | ------- | ----------- |
| name  | StringField | varchar | true        |
