# vue-tags-input

A tags input component for Vue 3 with autocompletion, custom validation, templating and much more

Forked from [@johmun/vue-tags-input](https://www.npmjs.com/package/@johmun/vue-tags-input), which you should use instead if your project is on Vue 2. 

[Demo & Docs](http://www.vue-tags-input.com) (for the original version)

## Features

* No dependencies
* Custom validation rules
* Hooks: Before adding, Before deleting ...
* Edit tags after creation
* Fast setup
* Works with Vuex
* Small size: 34kb minified (css included) | gzipped 9kb
* Autocompletion
* Many customization options
* Own templates
* Delete tags on backspace
* Add tags on paste
* Examples & Docs

## Install

NPM
```
npm install @fujiechen/vue3-tags-input
```

CDN
```
<script src="https://unpkg.com/@fujiechen/vue3-tags-input/dist/vue-tags-input.js"></script>
```

## Usage

```html
<template>
  <div>
    <vue-tags-input
      v-model="tag"
      :tags="tags"
      @tags-changed="newTags => tags = newTags"
    />
  </div>
</template>
```

```javascript
<script>
import VueTagsInput from "@fujiechen/vue3-tags-input";

export default {
  components: {
    VueTagsInput,
  },
  data() {
    return {
      tag: '',
      tags: [],
    };
  },
};
</script>
```

## Migration From Vue 2

This version is faithful to the original spec. The only thing you'll have to change is replacing any usages of `tags.sync` with `vmodel:tags` in the props

## License

[MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2023 Fujie Chen
