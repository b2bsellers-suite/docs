# How to build the b2b-platform (vue.js)

At B2Bsellers, we use dockware.io for local development. We can only recommend it to everyone. However, it doesn't matter if you use Dockware, Docker or something else.

Just execute the following code in the Shopware root folder:

```bash
bin/console b2b:platform:build
```

{% hint style="info" %}
Of course you need **Node.js** (see [Requirements](../../user-guide/setup/requirements.md)) to run the [watcher ](how-to-start-the-b2b-platform-vue.js-watcher.md)and the build command.
{% endhint %}
