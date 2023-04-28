# EmployeeCustomer

Table-name: b2b\_employee\_customer

Die EmployeeCustomer Entity ist die Mapping-Tabelle zwischen Customer und Employee. Bedeutet mit dieser Tabelle kann man einen Employee zu einem Kunden zuordnen, sodass ein Employee sich für den Kunden einloggen kann. Jede Employee kann somit bei jedem Kunden eine andere Rolle und Rechte haben.

#### Plugin

{% content-ref url="../../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Tabellen Spalten

| Field        | Class          | Typ      | Is required |
| ------------ | -------------- | -------- | ----------- |
| id           | IdField        | binary   | true        |
| customerId   | FkField        | binary   | true        |
| employeeId   | FkField        | binary   | true        |
| admin        | BoolField      | tinyint  | false       |
| roleId       | FkField        | binary   | false       |
| customFields | CustomFields   | json     | false       |
| updatedAt    | UpdatedAtField | Datetime | false       |
| createdAt    | CreatedAtField | Datetime | true        |

Vorsicht: Wenn EmployeeCustomer Admin ist, darf er keine Role zugewiesen bekommen.

### Associations

| Field    | Entity             | Class                     |
| -------- | ------------------ | ------------------------- |
| customer | CustomerEntity     | ManyToOneAssociationField |
| employee | EmployeeEntity     | ManyToOneAssociationField |
| role     | EmployeeRoleEntity | ManyToOneAssociationField |
