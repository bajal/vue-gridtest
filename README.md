# Vue Grid
#### Testing out Vue setup with webpack

> Vue.js project with Bootstrap support

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


### Vue Links

* https://vuejs.org/v2/guide/#Getting-Started
* https://bootstrap-vue.js.org/docs/components/form-input
* https://medium.com/codingthesmartway-com-blog/vue-js-2-quickstart-tutorial-2017-246195cfbdd2
* http://jsfiddle.net/7nxhygLp/


### Features in Vue:
* Reactive Interfaces - https://vuejs.org/v2/guide/reactivity.html (data and template bind)
* Declarative Rendering
* Data Binding
* Directives
* Template Logic
* Components
* Event Handling
* Computed Properties —— To bind transformed elements out of 'data'
* CSS Transitions and Animations
* Filters
* very small in size (only 17 kB)

To setup:
```
$ npm install -g vue-cli
$ vue init webpack vueapp01
$ cd vueapp01
$ npm install
$ npm run dev
```

###### index.html -> Starting point, 'app' is the placeholder
###### main.js -> Where Vue is initialized and routes are setup.
new Vue({
  el: '#app',
  router,
  template: '<App/>',
  components: { App }
})

###### App.vue - The component. Which is split into:
```
<template></template>: Component's template code
<script></script>: Component's script code
<style></style>: Component' CSS code
```

