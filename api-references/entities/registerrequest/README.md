# RegisterRequest

Table-name: b2b\_customer\_register\_request

#### Plugin

{% content-ref url="../../../user-guide/configuration-of-purchasable-addons/register-requests-wip.md" %}
[register-requests-wip.md](../../../user-guide/configuration-of-purchasable-addons/register-requests-wip.md)
{% endcontent-ref %}

### Table columns

| Field                         | Class          | Type     | Is required |
| ----------------------------- | -------------- | -------- | ----------- |
| id                            | IdField        | binary   | true        |
| autoIncrement                 | IntField       | int      | false       |
| requestedCustomerGroupId      | FkField        | binary   | false       |
| salesChannelId                | FkField        | binary   | false       |
| languageId                    | FkField        | binary   | false       |
| company                       | StringField    | varchar  | false       |
| presentCustomerNumber         | StringField    | varchar  | false       |
| companyEmail                  | StringField    | varchar  | false       |
| addressXXX                    | StringField    | varchar  | false       |
| title                         | StringField    | varcahr  | false       |
| salutationId                  | FkField        | binary   | false       |
| firstName                     | StingField     | varchar  | false       |
| lastName                      | StringField    | varchar  | false       |
| vatIds                        | JsonField      | json     | false       |
| doubleOptInRegistration       | BoolField      | tinyint  | false       |
| affiliateCode                 | StringField    | varchar  | false       |
| newsletter                    | BoolField      | tinyint  | false       |
| campaignCode                  | StringField    | varchar  | false       |
| remoteAddress                 | StringField    | varchar  | false       |
| tagIds                        | JsonField      | json     | false       |
| employeeTitle                 | StringField    | varchar  | false       |
| employeeEmail                 | StringField    | varchar  | false       |
| employeeSalutationId          | FkField        | binary   | false       |
| employeeFirstName             | StringField    | varchar  | false       |
| employeeLastName              | StringField    | varchar  | false       |
| employeePassword              | StringField    | varchar  | false       |
| employeeCustomFields          | JsonField      | json     | false       |
| legacyEncoder                 | StringField    | varchar  | false       |
| addressCountryId              | FkField        | binary   | false       |
| addressCountryStateId         | FkField        | binary   | false       |
| addressCompany                | StringField    | varchar  | false       |
| addressDepartment             | StringField    | varchar  | false       |
| addressSalutationId           | FkField        | binary   | false       |
| addressTitle                  | StringField    | varchar  | false       |
| addressFirstName              | StringField    | varchar  | false       |
| addressLastName               | StringField    | varchar  | false       |
| addressStreet                 | StringField    | varchar  | false       |
| addressZipCode                | StringField    | varchar  | false       |
| addressCity                   | StringField    | varchar  | false       |
| addressVatId                  | StringField    | varchar  | false       |
| addressPhoneNumber            | StringField    | varchar  | false       |
| addressAdditionalAddressLine1 | StringField    | varchar  | false       |
| addressAdditionalAddressLine2 | StringField    | varchar  | false       |
| addressCustomFields           | JsonField      | json     | false       |
| shopCustomerId                | FkField        | binary   | false       |
| statusId                      | FkField        | binary   | false       |
| customFields                  | CustomFields   | json     | false       |
| updatedAt                     | UpdatedAtField | Datetime | false       |
| createdAt                     | CreatedAtField | Datetime | true        |
