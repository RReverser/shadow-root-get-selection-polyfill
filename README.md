# ShadowRoot.getSelection Polyfill

Provides missing shadowRoot.getSelection implementation in browsers that need it.

The fix was sparked by an attempt to solve an issue with [prosemirror in Shadow Dom](https://github.com/ProseMirror/prosemirror/issues/476) and was inspired by [changes made to support Shadow DOM in quilljs](https://github.com/arsnebula/quill/commit/a6489a626f0e5d186ea9114d64efd0a3e1c44186#diff-ae237139107d046c67dc8622d25bace9).

Current browsers that do not provide a `shadowRoot.getSelection` implementation (Firefox! Safari!) return an appropriate value from `document.getSelection`.

Safari hasn't moved on this for [2 years](https://bugs.webkit.org/show_bug.cgi?id=163921), and the [GoogleChromeLabs polyfill](https://github.com/GoogleChromeLabs/shadow-selection-polyfill) doesn't actually address the problem.

## Installation

```
npm install shadow-root-get-selection-polyfill
```

or

```
yarn add shadow-root-get-selection-polyfill
```

## Usage

```js
import { patch } from 'shadow-root-get-selection-polyfill';
patch();
```
