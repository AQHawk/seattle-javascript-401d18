![cf](http://i.imgur.com/7v5ASc8.png) 23: Components and Routing
===

## Daily Plan
* Notes
  - Anything top of mind
  - Whiteboarding 'verification': At 30 minutes, please seek approval on current state, and then move on.
  - Don't forget the 15 minute rule... 

* Code Review _Build out the Reddit Search App_
* React Router _Introduction to client-side routing with ReactJS_
* Component Composition _Modularizing our front-end code base into reusable parts_

* Trees _Traversal methods: How to we navigate our tree data structure_

* Lab Preview _Build a notes app: Part 1_
* Whiteboard Challenge _Using your traversal methods, add a new node to the Tree_

----

## Learning Objectives
* students will be able to create front end routes through the use of `react-router-dom`
* students will be able to restructure their applications to use modular components
* students will be able to differentiate between view state and application state
* students will be able to lift application state to better control one way data flow

## Resources
* read [es6 modules](https://hacks.mozilla.org/2015/08/es6-in-depth-modules/)
* read [react-router-dom philosophy](https://reacttraining.com/react-router/web/guides/philosophy)
* read [lifting state up](https://facebook.github.io/react/docs/lifting-state-up.html)
* skim [mdn import](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import)
* skim [mdn export](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export)

## Overview
#### Front End React Routing
* the defacto routing library for react web applications is `react-router-dom`
  * this manages switching between components (based off of state or the window location) while controlling the browser history API
  * the browser history API allows users to hit the back button and revert to the last route without re-rendering the page

#### Types of State
###### Application State
* application state is any state that represents the core data of your application
  * this represents all of your models - for example:
    * auth
    * user
    * profile
    * note
    * list
    * article
    * comment
    * etc, etc

###### View State
* view state is any state that has to do with how a specific component should look - for example:
  * input values
  * which menu item is focused
  * when to hide/show a section of the view
  * when a hamburger menu is open or closed
  * etc, etc

#### Lifting State
* data can only flow from parents to children - if more than one component needs to reflect the same changing data, that data must be managed higher on the tree by a mutual parent
* one solution to this problem is to lift all **application state** to the top of the app, enabling the entire app to share changing state
* **important note:** view state does not often have to be lifted.

#### ES6 modules
* ES6 now supports its own ability to define JS modules
* ES6 Modules are like commonJS modules, except that they are automatically strict-mode code, even if you don't write `use-strict`
* ES6 now uses `export` and `import` to define and load modules
