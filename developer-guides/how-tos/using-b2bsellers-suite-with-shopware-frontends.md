---
description: >-
  In this article, you'll learn how to integrate B2Bsellers Suite with Shopware
  frontends to create a fully customizable e-commerce platform. The combination
  of these tools allows you to take advantage
---

# Using B2Bsellers Suite with Shopware frontends

## Advantages of Shopware Frontends

Before we dive into the details, let's take a look at the reasons why Shopware frontends might be interesting for your project:

* Platform agnostic customization: Shopware Frontends provides a toolkit to develop customized storefronts regardless of the platform.
* Flexibility and customizability: This solution allows you to design the look and functionality of your online store according to your needs.

## The API-Driven and Headless Approach

Both [Shopware 6](https://www.shopware.com/de/) and [B2Bsellers Suite](https://www.b2b-sellers.com/) are API-Driven and can be run headless. Use the B2Bsellers [Store API routes](../../api-references/store-api/) to add custom functionality to your Shopware Frontends Project, whether in the product listing page, product detail page, or checkout.&#x20;



## Integration of B2Bsellers Suite into Shopware frontends

{% hint style="info" %}
These instructions also apply to other PWA applications or frameworks, because the procedure is the same.
{% endhint %}

<figure><img src="../../.gitbook/assets/B2Bsellers Suite for Shopware Frontends.png" alt=""><figcaption><p>Tada, here is the screen of the B2B platform</p></figcaption></figure>

#### It is so simple ...

<pre class="language-typescript"><code class="lang-typescript">// b2b-platform/[...all].vue

&#x3C;script lang="ts">
export default {
  name: "B2bPlatformPage",
};
&#x3C;/script>


&#x3C;script setup lang="ts">
const { isLoggedIn } = useUser();
const { apiInstance } = useShopwareContext();
const url = useRequestURL()
const { languageIdChain } = useSessionContext();

if (process.client &#x26;&#x26; !isLoggedIn.value) {
  // redirect to account page if user is logged in
  navigateTo({ path: "/account" });
}

const { t } = useI18n();

const platformScript = `B2bPlatform.Platform.initializePlatform({
  context: {
    app: {
      basePath: "${url.origin}",
      languageId: "${languageIdChain.value}",
      defaultLanguageId: "${languageIdChain.value}",
      plugins: {
        "B2bOffer":{
          "css":["${apiInstance.config.endpoint}\/bundles\/b2boffer\/\/storefront\/assets\/static\/css\/b2b-offer.css"],
          "js":["${apiInstance.config.endpoint}\/bundles\/b2boffer\/\/storefront\/assets\/static\/js\/b2b-offer.js"]
        },
        "B2bEmployeeBudgets":{
          "css":[],
          "js":["${apiInstance.config.endpoint}\/bundles\/b2bemployeebudgets\/\/storefront\/assets\/static\/js\/b2b-employee-budgets.js"]
        },
        "B2bCostCenter":{
          "css":[],
          "js":["${apiInstance.config.endpoint}\/bundles\/b2bcostcenter\/\/storefront\/assets\/static\/js\/b2b-cost-center.j"]
        },
        "B2bProductSubscription":{
          "css":["${apiInstance.config.endpoint}\/bundles\/b2bproductsubscription\/\/storefront\/assets\/static\/css\/b2b-product-subscription.css"],
          "js":["${apiInstance.config.endpoint}\/bundles\/b2bproductsubscription\/\/storefront\/assets\/static\/js\/b2b-product-subscription.js"]
        },
        "B2bSalesRepresentativeFastOrder":{
          "css":[],
          "js":["${apiInstance.config.endpoint}\/bundles\/b2bsalesrepresentativefastorder\/\/storefront\/assets\/static\/js\/b2b-sales-representative-fast-order.js"]
        },
        "B2bMobileSalesPortalApp":{
          "css":[],
          "js":["${apiInstance.config.endpoint}\/bundles\/b2bmobilesalesportalapp\/\/storefront\/assets\/static\/js\/b2b-mobile-sales-portal-app.js"]
        },
        "B2bEventManager":{
          "css":["${apiInstance.config.endpoint}\/bundles\/b2beventmanager\/\/storefront\/assets\/static\/css\/b2b-event-manager.css"],
          "js":["${apiInstance.config.endpoint}\/bundles\/b2beventmanager\/\/storefront\/assets\/static\/js\/b2b-event-manager.js"]
        }
      },
      taxState: "gross",
      activeFeatures: ["B2bBonusProgram","B2bProductRequest","B2bUrlAuthentication","B2bPdpVariantList","B2bProductLists"],
      restrictions: [{"extensions":[],"name":"salesRepresentativeLimit","value":5.0}],
    },
    api: {
      basePath: "${apiInstance.config.endpoint}/store-api/",
      accessKey: "${apiInstance.config.accessToken}"
    },
    customer: {
      storeApiToken: "${apiInstance.config.contextToken}"
    }
  }
});`;
&#x3C;/script>


&#x3C;template>
  &#x3C;div class="max-w-screen-xl mx-auto">
    &#x3C;div id="app">
      &#x3C;div class="b2b-platform-loader is--initial d-flex justify-content-center align-items-center">
        &#x3C;div class="spinner-border text-primary" role="status">
          &#x3C;span>Loading...&#x3C;/span>
        &#x3C;/div>
      &#x3C;/div>
    &#x3C;/div>

    &#x3C;component is="script" type="application/javascript" src="/b2b-platform/js/runtime.js">&#x3C;/component>
    &#x3C;component is="script" type="application/javascript" src="/b2b-platform/js/vendors-node.js">&#x3C;/component>
    &#x3C;component is="script" type="application/javascript" src="/b2b-platform/js/commons.js">&#x3C;/component>
    &#x3C;component is="script" type="application/javascript" src="/b2b-platform/js/app.js">&#x3C;/component>

<strong>   // Obviously, some libraries should be included as an NPM package.
</strong>    &#x3C;component is="script" src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous">&#x3C;/component>
    &#x3C;component is="script" src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-Fy6S3B9q64WdZWQUiU+q4/2Lc9npb8tCaSX9FK7E8HnRr0Jz8D6OP9dO5Vg3Q9ct" crossorigin="anonymous">&#x3C;/component>

    &#x3C;link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css" integrity="sha384-xOolHFLEh07PJGoPkLv1IbcEPTNtaed2xpHsD9ESMhqIYd0nLMwNLD69Npy4HI+N" crossorigin="anonymous">
    &#x3C;link rel="stylesheet" href="/b2b-platform/css/vendors-node.css">
    &#x3C;link rel="stylesheet" href="/b2b-platform/css/app.css">

    &#x3C;client-only>
    &#x3C;component is="script">
      {{platformScript}}
    &#x3C;/component>
    &#x3C;/client-only>
  &#x3C;/div>
&#x3C;/template>


</code></pre>

Feel free to use this code snippet in your Shopware Composable Frontends project.... Feel free to share your experience with Shopware frontends...

### A few useful hints and tasks for you:

* You may need to make s**ome customizations** during the integration. Note that **Bootstrap** is required for the B2B platform, and you may need to make styling adjustments to accommodate the **storefront styling**.
* **Hash tag URLs:** Make sure that hash tag URLs (e.g., "b2b\_platform/offer#overview") work reliably, as they can occasionally cause reloads.
* **Initializing addons:** load the "initializePlatform" addon manually, as this is also present in the normal Shopware storefront. However, you can copy it to avoid conflicts.
* Further development via **Watcher**: It is advisable to find a solution to further develop the B2B platform with a Watcher tool. Alternatively, you can customize the B2Bsellers Suite Watch command accordingly.
* **Do not use classic IFrames:** It is not recommended to develop the B2B platform using classic IFrames.

So that was our test with Shopware Composable Frontend. We are curious if you use Shopware Composable Frontends and how you can take your B2B business to the next level.
