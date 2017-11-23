
cd C:/xampp/htdocs/VueJS_PROJECTS/KanjaVueJS_GettingStarted

Vue Data and Methods
===============================
When a Vue instance is created, it adds all the properties found in its data object to Vue’s reactivity system. 
When the values of those properties change, the view will “react”, updating to match the new values.
When the data changes, the view re-render. 
It should be noted that properties in data are only reactive if they existed when the instance was created. 
That means if you add a new property, then changes to it will not trigger any view updates. 
If you know you’ll need a property later, but it starts out empty or non-existent, you’ll need to set some initial value



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




Instance Lifecycle Hooks
==============================
1. created
2. mounted
3. updated
4. destroyed.

new Vue({
  data: {
    a: 1
  },
  created: function () {
    // `this` points to the vm instance
    console.log('a is: ' + this.a)
  }
})


# git
``` bash
#
git init

#
git clone

# git-commit - Record changes to the repository
git commit
git commit -m "message"

# This line will add and commit all changed and added files to repository.
git add . && git commit -am "comment"
```

#ADDING FILES
``` bash
#
git add .
#
git add hello.py
#
git add Documentation/\*.txt
#
git add git-\*.txt
```
# git-status - Show the working tree status
``` bash
#
git status 
```

# Pushing to a remote
``` bash
#
git push  <REMOTENAME> <BRANCHNAME> 
```
# To push local changes to online repository.
``` bash
#To push local changes to online repository.
git push origin master
```
## How to
``` bash
#
git init
#
git add README.md
#
git commit -m "first commit"
#
git remote add origin https://github.com/CeasarMwangi/VueJS_GettingStarted.git
# Verifies the new remote URL
git remote -v
#
git push -u origin master

```

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

Checkout the [guide](http://.../.../) and [docs for vue-loader](http://.../...).

# Create a repo for a new project
``` bash
# Creates a directory for your project called "Hello-World" in your user directory
mkdir ~/Hello-World

# Changes the current working directory to your newly created directory
cd ~/Hello-World

# create a file, named blabla.html
touch blabla.html

# Sets up the necessary Git files
git init

# Stages your blabla.html file, adding it to the list of files to be committed
git add blabla.html

# Commits your files, adding the message 
git commit -m 'first committttt'

# Creates a remote named "origin" pointing at your GitHub repository
git remote add origin https://github.com/username/Hello-World.git

# Sends your commits in the "master" branch to GitHub
git push -u origin master

#creates a new project on GitHub with the name of current directory
git create -d "My new thing"
```
# @TODO: try it out
``` bash

#
git init

#
git add . && git commit -m "It begins."

#creates a new project on GitHub with the name of current directory
git create -d "My new thing"

#
git push origin master

# setting git globals
git config --global user.name "Your Name"
# setting git globals
git config --global user.email you@example.com

```

# Template Syntax
## Data binding
Data binding is text interpolation using the “Mustache” syntax {{}}
``` bash
#Data binding
<span>Message: {{ msg }}</span>

#one-time interpolations that do not update on data change using the v-once directive, 
NB: This also affects any binding on the same node:
<span v-once>This will never change: {{ msg }}</span>
```
##In order to output real HTML, use the v-html directive:
``` bash
#Using mustaches
p>Using mustaches: {{ rawHtml }}</p>

#Using v-html directive
<p>Using v-html directive: <span v-html="rawHtml"></span></p>
Using mustaches: <span style="color: red">This should be red.</span>
Using v-html directive: This should be red.

```
## Attributes
Mustaches cannot be used inside HTML attributes. Instead, use a v-bind directive:
<div v-bind:id="dynamicId"></div>
In the case of boolean attributes, where their mere existence implies true, v-bind works a little differently. In this example:
<button v-bind:disabled="isButtonDisabled">Button</button>
If isButtonDisabled has the value of null, undefined, or false, the disabled attribute will not even be included in the rendered <button> element.