# PasswordlessLogin

Table-name: b2b\_passwordless\_login

#### Plugin

{% content-ref url="../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Table columns

| Field          | Class          | Type     | Is required |
| -------------- | -------------- | -------- | ----------- |
| id             | IdField        | binary   | true        |
| hash           | StringField    | varchar  | true        |
| customerId     | FkField        | binary   | false       |
| employeeId     | FkField        | binary   | false       |
| updatedAtField | UpdatedAtField | Datetime | false       |
| createdAt      | CreatedAtField | Datetime | true        |

### Associations

| Field    | Entity         | Class                    |
| -------- | -------------- | ------------------------ |
| customer | CustomerEntity | OneToOneAssociationField |
| employee | EmployeeEntity | OneToOneAssociationField |
