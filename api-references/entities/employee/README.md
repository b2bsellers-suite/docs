# Employee

Table-name: b2b\_employee

Die Employee Tabelle ist die Tabelle für Einkaufende Mitarbeiter. Hier sind alle Informationen von Vorname, über E-Mail Adresse und Passwort zu finden. Wenn ein customer das Custom Field "TODO" gesetzt hat, dann darf sich für diesen Kunden nur ein Employee einloggen. Diese Employee E-Mail Adresse muss also uniq sein und darf nicht bei einem anderen Employee erneut vorkommen.

Die Verbindung zu den Kunden, für die der Mitarbeiter einkaufen kann, wird in der Entity EmployeeCustomer gemappt.

#### Plugin

{% content-ref url="../../../developer-guides/b2bsellers-core-plugin/" %}
[b2bsellers-core-plugin](../../../developer-guides/b2bsellers-core-plugin/)
{% endcontent-ref %}

### Tabellen Spalten

| Field              | Class          | Type     | Is required |
| ------------------ | -------------- | -------- | ----------- |
| id                 | IdField        | binary   | true        |
| password           | PasswordField  | varchar  | false       |
| email              | EmailField     | varchar  | true        |
| active             | BoolField      | tinyint  | false       |
| passwordActivation | StringField    | varchar  | false       |
| languageId         | FkField        | binary   | true        |
| title              | StringField    | varchar  | false       |
| salutationId       | FkField        | binary   | true        |
| firstName          | StringField    | varchar  | true        |
| lastName           | StringField    | varchar  | true        |
| department         | StringField    | varchar  | true        |
| phoneNumber        | StringField    | varchar  | false       |
| mobilePhoneNumber  | StringField    | varchar  | false       |
| preferredCuserId   | FkField        | binary   | false       |
| loginTarget        | StringField    | varchar  | false       |
| customFields       | CustomFields   | json     | false       |
| updatedAt          | UpdatedAtField | Datetime | false       |
| createdAt          | CreatedAtField | Datetime | true        |

### Associations

| Field             | Entity                  | Class                     |
| ----------------- | ----------------------- | ------------------------- |
| customers         | EmployeeCustomerEntity  | OneToOneAssociationField  |
| salutation        | SalutationEntity        | ManyToOneAssociationField |
| language          | LanguageEntity          | ManyToOneAssociationField |
| preferredCustomer | EmployeeCustomerEntitiy | ManyToOneAssociationField |
