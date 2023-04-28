---
description: Store-API Endpunkt für die Registrationsanfrage.
---

# Account Request

{% hint style="info" %}
Die Registrationsanfrage muss aktiviert und konfiguriert werden siehe: [Registrationsprozess](../../user-guide/configuration/registrationsprozess.md)
{% endhint %}

{% swagger baseUrl="" path="/store-api/account-request" method="post" summary="Send Account Request" %}
{% swagger-description %}
Dieser Endpunkt nimmt die Daten der Anfrage entgegen und gibt diese an ein Mail Event weiter
{% endswagger-description %}

{% swagger-parameter in="body" name="companyConfirmation" type="boolean" required="false" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="employee" type="array" required="false" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="company" type="array" required="false" %}

{% endswagger-parameter %}

{% swagger-response status="204" description="" %}
```
```
{% endswagger-response %}

{% swagger-response status="400" description="" %}
```
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}
