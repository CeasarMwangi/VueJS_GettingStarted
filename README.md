===============================
Vue Data and Methods
===============================
When a Vue instance is created, it adds all the properties found in its data object to Vue’s reactivity system. 
When the values of those properties change, the view will “react”, updating to match the new values.
When the data changes, the view re-render. 
It should be noted that properties in data are only reactive if they existed when the instance was created. 
That means if you add a new property, then changes to it will not trigger any view updates. 
If you know you’ll need a property later, but it starts out empty or non-existent, you’ll need to set some initial value


==============================
instance properties and methods
==============================
These are prefixed with $ to differentiate them from user-defined properties. For example:
var data = { a: 1 }
var vm = new Vue({
  el: '#example',
  data: data
})
vm.$data === data // => true
vm.$el === document.getElementById('example') // => true
// $watch is an instance method
vm.$watch('a', function (newValue, oldValue) {
  // This callback will be called when `vm.a` changes
})



==============================
Instance Lifecycle Hooks
1. created
2. mounted
3. updated
4. destroyed.
==============================
new Vue({
  data: {
    a: 1
  },
  created: function () {
    // `this` points to the vm instance
    console.log('a is: ' + this.a)
  }
})


==============================
--git
==============================
>git init
>git clone
>git commit

----------------------------
==ADDING FILES
----------------------------
>git add .
>git add Documentation/\*.txt
>git add git-*.sh

---------------------------------
git-status - Show the working tree status
---------------------------------
>git status 
==============================
==============================



==============================
==============================



==============================
==============================


# todo-app

> A Vue.js getting started project

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

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
