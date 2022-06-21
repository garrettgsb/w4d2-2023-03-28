## Learning Outcomes

### Web Pages
* What is the DOM?
  * What is the `document` object?
  * In what sense is it a "model?" A model of what?
* Why all this talk about trees?

### Manipulating Web Pages with "vanilla" Javascript
* How do you get Javascript into a webpage?
* How do you do stuff to HTML elements?
  - Select them
    - `getElementById`
    - `getElementsByTagName`
    - `getElementsByClassName`
    - `querySelectorAll`
  - Modify them
  - Iterate over them
  - Create new ones and add them to the DOM
  - Add interactivity to them with **event listeners**
* `document.ready`

#### Vanilla JS Survival kit:

* Grab an element: `document.querySelector('.tweet-container > header') /* some CSS selector */` (Or `querySelectorAll` if you want to get more than one)
* Create a new element from scratch: `document.createElement('div') /* Any HTML tag, as a string */`
* Attach an element to the DOM somewhere:
  * Select an element to nest it under: `const body = document.querySelector('body')`
  * Append it! `body.append(theElementIJustCreated)`
* Change the contents of an element: `element.innerHTML = <h2>New content</h2>` Can contain HTML!

### jQuery
* High level - What is jQuery?
* Why jQuery became popular
* Including jQuery in a project
  * CDNs - https://releases.jquery.com/
* The `jQuery()` function
* `$` What's this?
* `$(() => {});` What's this?
  * `document.ready(() =>{})` vs. `$(document).ready(() => {})` vs. `$(() => {})`

* Using jQuery in the console
* How do you do stuff to HTML elements with jQuery? (same stuff as above)
* `$('li')` vs. `$('<li>')`
* DOM nodes vs. jQuery objects
* How do you use the jQuery docs?
* Vanilla JS vs. jQuery (Why you might not need jQuery) https://github.com/nefe/You-Dont-Need-jQuery

### 04 - Handling Clicks

### 05 - Vampire Editor

* Use the provided `findVampire` method to hard-code adding an offspring to one of the vampires
* It fails; why?
* Next create a modal: Input, Create, Cancel
  * It opens when you click a Vampire

### 06 - Vampire Editor But It's jQuery

* Adding jQuery to a project
  * What's a CDN?
  * What's `min` (minification)?
* The `jQuery` function
  * The `$` alias
  * The three interfaces of the jQuery function:
    * `$('div')`
    * `$('<div>')`
    * `$(() => {})`
