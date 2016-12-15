# Top layer API


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## tl;dr

The top layer API would allow developers to add elements to the
[top layer](https://fullscreen.spec.whatwg.org/#top-layer)
programmatically.

When adding elements,
developers may optionally specify that they be added _modally_:
in this case,
everything _lower_ than the element in question 
(including lower elements in the top level)
would become
[inert](https://html.spec.whatwg.org/multipage/interaction.html#inert),
and the element would have a `::backdrop` pseudo-element.


```js
// Add `el` to top layer, pushing it on to the top. If it was already in the top layer,
// move it to the top of the top layer.
document.topLayer.add(el);

// Remove `el` from top layer, moving it back to its original position in the DOM.
// (Typically this is unlikely to be called; instead, developers would most likely
// hide or show the element.)
document.topLayer.remove(el);

// Adds `el` to the top layer, and additionally causes its ::backdrop pseudo-element to 
// be created, and all other page content, including other top layer content, to be `inert`.
document.topLayer.add(el, { modal: true });

// Fetches the read-only list of top layer elements in stack order, top-most first.
document.topLayer.stack();

```

## Top Layer

The
[top layer](https://fullscreen.spec.whatwg.org/#top-layer)
concept is described in the 
[Fullscreen API](https://fullscreen.spec.whatwg.org/),
and referred to in the
[`<dialog>` element specification](https://html.spec.whatwg.org/multipage/forms.html#the-dialog-element). 
This spec makes that concept directly accessible via a scripting API,
with one important change:
only elements added using the `modal` option have a `::backdrop` pseudo-element.





## Spec

### Use cases

- **Use case 1**

  Some info about use case 1.
  
  + Some bullets.
  -->


