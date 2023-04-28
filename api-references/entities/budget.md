# Budget

Table-name: b2b\_budget

| Field                  | Class          | Type     | Is required |
| ---------------------- | -------------- | -------- | ----------- |
| id                     | IdField        | binary   | true        |
| active                 | IntField       | int      | false       |
| periodType             | StringField    | varchar  | false       |
| sum                    | FloatField     | double   | false       |
| periodUsed             | FloatField     | double   | false       |
| restrictedCategories   | CustomFields   | json     | false       |
| customFields           | CustomFields   | json     | false       |
| internalComment        | StringField    | varchar  | false       |
| approvalEmployeeId     | FkField        | binary   | false       |
| notificationPercentage | IntField       | int      | false       |
| creatorUserId          | FkField        | binary   | false       |
| updatedAt              | UpdatedAtField | Datetime | false       |
| createdAt              | CreatedAtField | Datetime | true        |
