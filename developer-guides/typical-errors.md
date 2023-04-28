---
description: >-
  This page should help developers to easily solve and explain typical bugs we
  have noticed or had ourselves.
---

# Typical errors

### 1. \[webpack-cli] ModuleNotFoundError: Module not found: Error: Can't resolve 'prosemirror-keymap' TIPTAP&#x20;

This error can occur when running "b2b:platform:build"

1\. Go into path: **custom/plugins/b2bsellerscore/src/Resources/app/b2b\_platform**\
2\. Install dependencies with this command:&#x20;

```
npm i prosemirror-schema-list prosemirror-history prosemirror-dropcursor prosemirror-gapcursor prosemirror-keymap prosemirror-commands
```

Afterwards it should be possible to build our b2b platform.

### 2. Alternative:

```
// Quickfix, use specific npm version (dockware.io)
source ~/.bashrc
nvm install 16.15.1
```

More informations: [https://github.com/ueberdosis/tiptap/issues/3492](https://github.com/ueberdosis/tiptap/issues/3492)



