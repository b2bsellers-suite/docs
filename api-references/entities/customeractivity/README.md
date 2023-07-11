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

<table><thead><tr><th width="238.70829469599607">Field</th><th width="243.88498823361266">Entity</th><th>Class</th></tr></thead><tbody><tr><td>customer</td><td>CustomerEntity</td><td>ManyToOneAssociationField</td></tr><tr><td>employee</td><td>EmployeeEntity</td><td>ManyToOneAssociationField</td></tr><tr><td>type</td><td>MegaCustomerActivityTypeEntity</td><td>ManyToOneAssociationField</td></tr></tbody></table>
