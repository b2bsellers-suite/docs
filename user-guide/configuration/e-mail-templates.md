# E-Mail Templates

{% hint style="info" %}
**Get info about changed mail templates**\
\
It is good to know that in newer B2Bsellers Suite versions, adjustments have been made to the mail templates, but these are not automatically changed in your already installed versions when you update. This is because we do not know if they may have made adjustments to the mail template. However, you are welcome to look into the mail template files directly in B2Bsellers Core and copy the content.
{% endhint %}

The B2Bsellers Suite has created a separate mail template for each email sent in the standard, which can be edited normally in the Shopware Administration.

Each mail template is available in English and German and also in PLAIN and HTML. You have to add other languages yourself. All mail templates are automatically created in Shopware during installation and can then be edited.

You can also find some of the mail templates in the individual plugin descriptions (docs), but here is a list of sample mail templates.

### Employee invite mail

```
Hello,
You have been invited by your responsible company administrator on {{
salesChannel.name
}} to the company {{customer.company}}.
Please use the following link to join this company and set your password: {{activationUrl}}
```

### Password less login mail

```
{% raw %}
{% set user = customer %}
{% if not user %}{% set user = employee %}{% endif %}
{% endraw %}
Hello {{ user.firstName }} {{ user.lastName }},

To log into your account, click this link {{ passwordlessLoginUrl }}

The link is valid for 30 minutes. After the 30 minutes have passed, simply request a new link.
If you do not want to log in, please ignore this email.
```

### Account request form

#### Submitted data of registration request

```
Company name: {{ requestFormData.company.name }}
Vat ID: {{ requestFormData.company.vatId }}
Central email address:{{ requestFormData.company.email }}
Previous customer number:{{ requestFormData.company.customerNumber }}

Street + Street number: {{ requestFormData.company.street }}
Zip + Location: {{ requestFormData.company.zipcode }} {{ requestFormData.company.city }}
Country: {{ requestFormData.company.country.translated.name }}
```

#### Employee access

```
Salutation: {{ requestFormData.employee.salutation.translated.displayName }}
Email: {{ requestFormData.employee.email }}
First- & lastname: {{ requestFormData.employee.firstName }} {{ requestFormData.employee.lastName }}
```

... and many more mail templates

All available MailTemplates from the B2Bsellers CORE plugin can be found under the path: "b2bsellerscore/src/Setup/MailTemplates".
