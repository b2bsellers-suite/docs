# CollectionAccount

Table-name: b2b\_collection\_account

#### Plugin

{% content-ref url="../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Table columns

| Field           | Class          | Type     | Is required |
| --------------- | -------------- | -------- | ----------- |
| id              | IdField        | binary   | true        |
| number          | IntField       | integer  | false       |
| encoder         | StringField    | varchar  | false       |
| password        | StringField    | varchar  | false       |
| email           | StringField    | varchar  | false       |
| active          | BoolField      | tinyint  | false       |
| companyName     | StringField    | varchar  | false       |
| title           | StringField    | varchar  | false       |
| salutation      | StringField    | varchar  | false       |
| firstName       | StringField    | varchar  | false       |
| lastName        | StringField    | varchar  | false       |
| internalComment | LongTextField  | text     | false       |
| creatorId       | FkField        | binary   | false       |
| updatedAt       | UpdatedAtField | Datetime | false       |
| createdAt       | CreatedAtField | Datetime | true        |
