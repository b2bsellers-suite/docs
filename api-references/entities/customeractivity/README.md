# CustomerActivity

Table-name: b2b\_customer\_activity

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/b2boffers.md" %}
[b2boffers.md](../../../user-guide/configuration-of-purchasable-addons/b2boffers.md)
{% endcontent-ref %}

### Table columns

| Field          | Class       | Type    | Is required |
| -------------- | ----------- | ------- | ----------- |
| id             | IdField     | binary  | true        |
| referenceType  | StringField | varchar | false       |
| referenceId    | FkField     | binary  | false       |
| customerId     | FkField     | binary  | true        |
| employeeId     | FkField     | binary  | false       |
| activityTypeId | FkField     | binary  | false       |
| comment        | FkField     | varchar | false       |

### Associations

| Field    | Entity                         | Class                     |
| -------- | ------------------------------ | ------------------------- |
| customer | CustomerEntity                 | ManyToOneAssociationField |
| employee | EmployeeEntity                 | ManyToOneAssociationField |
| type     | MegaCustomerActivityTypeEntity | ManyToOneAssociationField |
