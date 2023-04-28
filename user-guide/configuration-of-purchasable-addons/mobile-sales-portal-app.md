# Mobile sales portal (app)

{% hint style="warning" %}
This feature is already included as source code in B2BsellersCore v1.0, but this is marked as BETA because the APP is currently under development. We are planning a release in Q3 2023. If you want to become a beta tester, contact us!
{% endhint %}

### What can the mobile app do for Sales representatives?

Make it as easy as possible for your Sales representatives to use digital devices for order entry, quoting, or customer service.

Our app enables sales teams to place orders on the go on behalf of customers, fill customer shopping carts, view quotes and orders, and other useful features.

Be excited.

Contact by mail: [sales@b2b-sellers.com](mailto:sales@b2b-sellers.com)

{% hint style="info" %}
The app will be available in the **iOS app store** as well as the **Android store**.&#x20;



It is developed on [Flutter](https://flutter.dev/).
{% endhint %}

### How to install the Addon?

It is easy to activate via the license settings. In some cases (e.g. if you have installed Shopware via Composer) you have to execute "composer install" in the addon itself, because here a QR Code Package is needed.

```
cd custom/plugins/b2bsellerscore
cd addons/B2bMobileSalesPortalApp/
composer install
```

{% hint style="info" %}
If you run "composer install" inside the B2BsellersCore, it will automatically install the packages inside the MobilesSalesPortalApp.
{% endhint %}
