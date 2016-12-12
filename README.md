# Top layer API


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## tl;dr

```js
// Add `el` to top layer, pushing it on to the top. If it was already in the top layer,
// move it to the top of the top layer.
document.addToTopLayer(el);

// Remove `el` from top layer, moving it back to its original position in the DOM.
// (Typically this is unlikely to be called; instead, developers would most likely
// hide or show the element.)
document.removeFromTopLayer(el);

// Adds `el` to the top layer, and additionally causes its ::backdrop pseudo-element to 
// be created, and all other page content, including other top layer content, to be `inert`.
document.addToTopLayer(el, { modal: true }); 

```
<!--


## Background

## Spec

### Use cases

- **Use case 1**

  Some info about use case 1.
  
  + Some bullets.
  -->


