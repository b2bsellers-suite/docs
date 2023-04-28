# RegisterRequestActivity

Table-name: b2b\_customer\_register\_request\_status

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/register-requests-wip.md" %}
[register-requests-wip.md](../../../user-guide/configuration-of-purchasable-addons/register-requests-wip.md)
{% endcontent-ref %}

### Table columns

| Field                        | Class          | Type     | Is required |
| ---------------------------- | -------------- | -------- | ----------- |
| id                           | IdField        | binary   | true        |
| b2bCustomerRegisterRequestId | FkField        | binary   | false       |
| type                         | StringField    | varchar  | false       |
| text                         | StringField    | varchar  | false       |
| updatedAt                    | UpdatedAtField | Datetime | false       |
| createdAt                    | CreatedAtField | Datetime | true        |
