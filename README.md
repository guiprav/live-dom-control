Live DOM Control
================

Non-intrusively keep track of elements being added, removed, or modified in the DOM.

This library requires jQuery 1.8 or greater. This dependency may be removed in the future, but since I use jQuery on all my projects I just used it here too. Patches welcome.

`dom_control(selector, handler)` will call `handler(event, element, attribute)` every time an element matching `selector` is added to or removed from the DOM, and every time such an element has one of its attributes modified.

In `handler(event, element, attribute, old_value)`:

* `event` is either `'added'`, `'removed'`, or `'mutated'`.
* `element` is the `DOMElement` that produced the event.
* `attribute` is the name of the attribute if `event` === `'mutated'`, or `undefined` otherwise.
* `old_value` is the old attribute value if `event` === `'mutated'`, or `undefined` otherwise.

Demo: [https://rawgithub.com/n2liquid/libtile/demo-1/demo.html.](https://rawgithub.com/n2liquid/libtile/demo-1/demo.html)

---

live-dom-control is free software under the terms of the GPLv3 license, a copy of which can be found in [COPYING.](COPYING) This means that all JavaScript code on your website directly or indirectly relying on live-dom-control must be licensed under a [GPLv3-compatible license.](https://www.gnu.org/licenses/license-list.html#GPLCompatibleLicenses) Some free software licenses are unfortunately [not GPLv3-compatible.](https://www.gnu.org/licenses/license-list.html#GPLIncompatibleLicenses)

This is important in order to perpetuate free software and combat all forms of non-free software. Learn more about GPLv3 on [gnu.org/licenses.](https://www.gnu.org/licenses/quick-guide-gplv3.html)
