# Employee

{% swagger method="post" path="/store-api/employees" baseUrl="" summary="Send Employees list" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="get" path="/store-api/employee/{id}" baseUrl="" summary="Retrieve Employees" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" required="true" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="/store-api/employee" baseUrl="" summary="Create Employees" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="patch" path="/store-api/employee/{id}" baseUrl="" summary="Update Employees" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" required="true" %}

{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="/store-api/employee/add" baseUrl="" summary="Add Employee" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="delete" path="/store-api/employee/{id}" baseUrl="" summary="Delete Employee" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" required="true" %}

{% endswagger-parameter %}
{% endswagger %}
