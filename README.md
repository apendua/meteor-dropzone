meteor-dropzone
===============

To use call `$.dropzone()` on all nodes where you want to add `dropzone`.
For example, if your template looks like this

```html
<template name="myDropzoneTemplate">
  <div class="droparea"></div>
</template>
```

you'll need to use your template `rendered` hook:

```javascript
Template.myDroparaTemplate.rendered = function () {
  $(this.find('.droparea')).dropzone();
}
```

To define the `drop` event use:

```javascript
Template.myTemplate.events({
  'drop .dropzone': function () {
    // my drop callback
  }
});
```
