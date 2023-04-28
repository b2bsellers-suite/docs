# Customer Activity

{% swagger method="get" path="/store-api/customer-activity/{id}" baseUrl="" summary="Retrieve Customer Activity" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" required="true" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="delete" path="/store-api/customer-activity/{id}" baseUrl="" summary="Delete Customer Activity" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" required="true" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="get" path="/store-api/customer-activity" baseUrl="" summary="Retrieve Customer Activity list" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="post" path="/store-api/customer-activity/list" baseUrl="" summary="List Customer Activity " %}
{% swagger-description %}
list activities
{% endswagger-description %}

{% swagger-parameter in="header" name="authorization" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="/store-api/customer-activity" baseUrl="" summary="Create Customer Activity" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="put" path="/store-api/customer-activity/" baseUrl="" summary="Update Customer Activity" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}
