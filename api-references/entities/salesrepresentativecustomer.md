# SalesRepresentativeCustomer

Table-name: b2b\_sales\_representative\_customer

#### Plugin

{% content-ref url="../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Table columns

<table><thead><tr><th>Field</th><th width="200.33333333333331">Class</th><th>Type</th><th>Is required</th></tr></thead><tbody><tr><td>id </td><td>IdField</td><td>binary</td><td>true</td></tr><tr><td>salseRepId</td><td>FkField</td><td>binary</td><td>true</td></tr><tr><td>customerId</td><td>FkField</td><td>binary</td><td>true</td></tr><tr><td>updatedAt</td><td>UpdatedAtField</td><td>Datetime</td><td>false</td></tr><tr><td>createdAt</td><td>CreatedAtField</td><td>Datetime</td><td>true</td></tr></tbody></table>

### Associations

| Field    | Entity         | Class                     |
| -------- | -------------- | ------------------------- |
| customer | CustomerEntity | ManyToOneAssociationField |
