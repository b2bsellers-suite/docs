# PaymentCondition

Table-name: b2b\_payment\_condition

#### Plugin

{% content-ref url="../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Table columns

| Field              | Class          | Type     | Is required |
| ------------------ | -------------- | -------- | ----------- |
| id                 | IdField        | binary   | true        |
| number             | StringField    | varchar  | false       |
| description        | StringField    | varchar  | false       |
| debtCollectionType | StringField    | varchar  | false       |
| netCondition       | Stringfield    | varchar  | false       |
| skontoCondition1   | StringField    | varchar  | false       |
| skontoCondition2   | StringField    | varchar  | false       |
| skontoPercent1     | FloatField     | double   | false       |
| skontoPercent2     | FloatField     | double   | false       |
| updatedAt          | UpdatedAtField | Datetime | false       |
| createdAt          | CreatedAtField | Datetime | true        |
