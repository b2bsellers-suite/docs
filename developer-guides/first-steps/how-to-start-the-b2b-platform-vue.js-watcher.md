# How to start the b2b-platform vue.js watcher

As soon as you log in as a customer employee or as a sales agent, the B2B-Platform opens - that's what we call this Vue.js interface.

{% hint style="success" %}
since B2BsellersCore Version 0.9.4, the password is not longer needed. It is enough to set the email-address of the employee
{% endhint %}

As soon as you log in as a customer employee, the B2B-Platform opens - that's what we call this Vue-Js interface.

You can extend or overwrite this B2B platform according to your requirements.\
You can find helpful links here: [How to add „Menü Item“ on B2BPlattform](../../user-guide/configuration/how-to-add-menue-item-on-b2bplattform.md)

But before you can start developing you have to start the Vue.js Watcher.\
In your local installation (we recommend [DOCKWARE.IO](http://dockware.io/)) in the Shopware root folder you can use the following command to start the Vue.js Watcher:

{% hint style="info" %}
Tip: When executing the watch command, the command goes through all folders and indexes the main.js files. So if you are developing an extension, start the watcher only after creating the main.js file in the _"{pluginRoot}/src/Resources/app/b2b\_platform/"_ folder.
{% endhint %}

#### Console command:

```
bin/console b2b:platform:watch <email>
```

#### Command example for Henk Becker (Employee at Ektek GmbH - Testdata)

```shell
bin/console b2b:platform:watch henk.becker@ektek.com 
```

#### Command example for Markus Bauer (Sales Representative at Shopowner - Testdata)

```shell
bin/console b2b:platform:watch m.bauer@luxon.de
```

After entering the command you get prompted to select the wanted sales channel and domain (if multiple are available).

```shell
Please select a sales channel:
  [0] Storefront | 3599498813f14f1a8abe0deb0e12d18
  [1] Headless | 98432def39fc4624b33213a56b8c944d
```

```shell
Please select a domain:
  [0] http://localhost/de | Deutsch | 9a088b6be800412fb71ca53e96ba7778
  [1] http://localhost | English | 9d6dd97cee0548d99bcafbc65126f46a
```

The Vue.js watcher starts after the necessary selections and can be opened under the port 9998 or the link http://localhost:9998/b2b\_platform/ after being compiled successfully.

```shell
  App running at:
  - Public URL: http://localhost:9998/b2b_platform/

  To build for production , run bin/console b2b:platform:build
```
