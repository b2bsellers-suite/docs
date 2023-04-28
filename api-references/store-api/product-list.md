# Product List

{% swagger method="post" path="/store-api/product-lists" baseUrl="" summary="Product Lists" %}
{% swagger-description %}
Dieser Endpunkt... ToDo
{% endswagger-description %}
{% endswagger %}

{% swagger method="post" path="/store-api/product-lists/create" baseUrl="" summary="Create Product Lists " %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/store-api/product-lists/detail/{id}" baseUrl="" summary="Retrieve Product List" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" required="true" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="delete" path="/store-api/product-lists/{id}" baseUrl="" summary="Delete Product Lists" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="items" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="patch" path="/store-api/product-lists/{id}" baseUrl="" summary="Update Porduct Lists" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="delete" path="/store-api/product-lists/product/{id}/{productListId}" baseUrl="" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="path" name="productListId" type="String" required="true" %}

{% endswagger-parameter %}
{% endswagger %}
