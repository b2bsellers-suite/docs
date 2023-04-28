# RegisterRequestStatus

Table-name: b2b\_customer\_register\_request\_status

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/register-requests-wip.md" %}
[register-requests-wip.md](../../../user-guide/configuration-of-purchasable-addons/register-requests-wip.md)
{% endcontent-ref %}

### Table columns

| Field       | Class           | Type     | Is required |
| ----------- | --------------- | -------- | ----------- |
| id          | IdField         | binary   | true        |
| name        | TranslatedField | varchar  | false       |
| description | TranslatedField | varchar  | false       |
| updatedAt   | UpdatedAtField  | Datetime | false       |
| createdAt   | CreatedAtField  | Datetime | true        |

### Associations

| Field                              | Entity                                 | Class                        |
| ---------------------------------- | -------------------------------------- | ---------------------------- |
| b2bCustomerRegisterRequestStatusId | RegisterRequestStatusTranslationEntity | TranslationsAssociationField |

### RegisterRequestStatusTranslation

| Field       | Class       | Type    | Is required |
| ----------- | ----------- | ------- | ----------- |
| name        | StringField | varchar | true        |
| description | StringField | varchar | true        |
