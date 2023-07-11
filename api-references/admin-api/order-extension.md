---
description: >-
  You can access the employee and sales representative`s information on orders
  from the new b2bOrderExtension:
---

# Order Extension

### Associations to get the data via the API or the DAL.

Associations _via DAL_

```
$criteria->addAssociations([
    'b2bOrderExtension.employee',
    'b2bOrderExtension.salesRepresentative'
]);
```

Associations _via API_

```
{
  associations: {
    b2bOrderExtension: {
      associations: {
        employee: {},
        salesRepresentative: {}
      }
    }
  }
}
```

**The data can then be found under the "extensions" as "b2bOrderExtension".**

```
{
  id: "...",
  orderNumber: "...",
  ...,
  extensions: {
    b2bOrderExtension: {
      employeeId: "...",
      salesRepresentativeId: "...",
      employee: {...},
      salesRepresentative: {...},
      ...
    }
  }
}
```
