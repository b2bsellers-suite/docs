---
description: Configuration of the registration process
---

# Registration process

### Send welcome mail if flag exists

When updating or creating a client, if the flag \*\*\*\* _"\_sendWelcomeMail"_ is sent with, a welcome email will be sent

{% hint style="danger" %}
The customer must have set the additional field "b2b\_platform\_access".
{% endhint %}

### Send welcome mail when creating customer

Bei jeder Erstellung eines Kunden wird eine Willkommens-Email versendet

{% hint style="danger" %}
Der Kunde muss das Zusatzfeld "b2b\_platform\_access" gesetzt haben.
{% endhint %}

### Registration Anfrageformular statt Anmeldung

Geschäftskunden können sich nicht mehr normal Registrieren, stattdessen werden die Formulardaten via E-Mail an den Shopbetreiber gesendet.

### Gewerbebestätigung in der Registration

Geschäftskunden müssen durch eine Checkbox bestätigen dass Sie auch wirklich ein Gewerbe betreiben, das betrifft nur das Formular in der Option "Registration Anfrageformular statt Anmeldung".

### Kunden werden als B2b-Kunden registriert

Bei Kunden welche sich über die Registration anmelden wird automatisch das _"b2b\_platform\_access"_ gesetzt und ein dazugehöriger Mitarbeiter wird erstellt.
