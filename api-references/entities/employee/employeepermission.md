# EmployeePermission

Table-name: b2b\_employee\_permission

#### Plugin

{% content-ref url="../../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Tabellen Spalten

| Field     | Class           | Type     | Is required |
| --------- | --------------- | -------- | ----------- |
| id        | IdField         | binary   | true        |
| key       | StringField     | varchar  | true        |
| name      | TranslatedField | varchar  | false       |
| updatedAt | UpdatedAtField  | DateTime | false       |
| createdAt | CreatedAtField  | DateTime | true        |

### Associations

| Field                    | Entity                              | Class                        |
| ------------------------ | ----------------------------------- | ---------------------------- |
| megaEmployeePermissionId | EmployeePermissionTranslationEntity | TranslationsAssociationField |

### EmployeePermissoinTranslation

| Field | Class       | Type    | Is required |
| ----- | ----------- | ------- | ----------- |
| name  | StringField | varchar | true        |
