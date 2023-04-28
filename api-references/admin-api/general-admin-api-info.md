# General Admin-API Info

The Admin API is used to create integrations with external systems and the API provides CRUD operations for each entity. For all B2Bsellers entities there are automatically created API endpoints from Shopware 6.

This makes the B2Bsellers Suite as well as Shopware 6 completely API-driven.

For more information, please take a look at the shopware 6 doku:&#x20;

[Integrations / API](https://developer.shopware.com/docs/guides/integrations-api)

## Bulk Payloads

You want to transfer multiple items to Shopware 6 at once, then you can also use SYNC API on all Shopware 6 entities.

For more information, please refer to the official Shopware 6 documentation:

{% hint style="info" %}
More Information: \
[https://shopware.stoplight.io/docs/admin-api/faf8f8e4e13a0-bulk-payloads ](https://shopware.stoplight.io/docs/admin-api/faf8f8e4e13a0-bulk-payloads)
{% endhint %}

#### An excerpt from the Shopware doc:

The Sync API is an extension of the Admin API that allows you to perform multiple write operations (create/update and delete) at the same time. All entities that can be written via the Admin API can also be written via the Sync API.

The endpoint is located at

```
/api/_action/sync
```

and expects payloads via POST and Content-Type: application/json.

### Example Request

```json
// POST /api/_action/sync

{
    "write-tax": {
        "entity": "tax",
        "action": "upsert",
        "payload": [
            { "name": "tax-1", "taxRate": 16 },
            { "name": "tax-2", "taxRate": 15 }    
        ]
    },
    "write-category": {
        "entity": "category",
        "action": "upsert",
        "payload": [
            { "name": "category-1" },
            { "name": "category-2" }
        ]
    },
    "write-country": {
        "entity": "country",
        "action": "upsert",
        "payload": [
            { "name": "country-1" },
            { "name": "country-2" }
        ]
    }
}


// Response
{
    "success": true,
    "data": {
        "write-tax": {
            "result": [
                {
                    "entities": {
                        "tax": ["bd59bcc0ceaa4acbbbb9e5e9d22b0312"]
                    }
                },
                {
                    "entities": {
                        "tax": ["38bfe5140d58429a840190c6ed43f0c4"]
                    }
                }
            ]
        },
        "write-category": {
            "result": [
                {
                    "entities": {
                        "category": ["0a2275ff38a747069fce697bc2582bdc"],
                        "category_translation": [
                            { "categoryId": "0a2275ff38a747069fce697bc2582bdc", "languageId": "2fbb5fe2e29a4d70aa5854ce7ce3e20b" }
                        ]
                    }
                },
                {
                    "entities": {
                        "category": ["8df6114ba9c84116b6011d6b9ce1fa3a"],
                        "category_translation": [
                            { "categoryId": "8df6114ba9c84116b6011d6b9ce1fa3a", "languageId": "2fbb5fe2e29a4d70aa5854ce7ce3e20b" }
                        ]
                    }
                }
            ]
        },
        "write-country": {
            "result": [
                {
                    "entities": {
                        "country": ["91738c2ee74a464e8ffe4f1d572449b3"],
                        "country_translation": [
                            { "countryId": "91738c2ee74a464e8ffe4f1d572449b3", "languageId": "2fbb5fe2e29a4d70aa5854ce7ce3e20b" }
                        ]
                    }
                },
                {
                    "entities": {
                        "country": ["69b2d17d04364620ad9ded6b01f471cd"],
                        "country_translation": [
                            { "countryId": "69b2d17d04364620ad9ded6b01f471cd", "languageId": "2fbb5fe2e29a4d70aa5854ce7ce3e20b" }
                        ]
                    }
                }
            ]
        }
    }
}

```
