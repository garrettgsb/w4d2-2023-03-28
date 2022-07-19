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
* Document readiness

#### Vanilla JS Survival kit:

* Grab a collection of elements: `document.querySelectorAll('button')` (Grab all of the `<button>` tags on the page)
* Grab an element: `document.querySelector('.tweet-container > header') /* some CSS selector */` (Grab the first `<header>` element inside an element with the class `.tweet-container`)
* Create a new element from scratch: `document.createElement('div') /* Any HTML tag, as a string */`
* Attach an element to the DOM somewhere:
  * Select an element to nest it under: `const body = document.querySelector('body')`
  * Append it! `body.append(theElementIJustCreated)`
* Change the contents of an element: `element.innerHTML = <h2>New content</h2>` Can contain HTML!
* Get rid of an element: `element.remove()`
* Hey, that's BREAD! ☝️
* Attach an event to an element: `helpButton.addEventListener('click', () => alert('Help is on the way!'))`

### 04 - Handling Events

Another major feature that the DOM provides is the ability to notice when Events happen, and to bind actions to those Events.
Such a function is called an **Event Handler**.

Events also have targets. Most of the time, those targets are DOM Elements.
Attaching an Event to an Element is referred to as **registering an event**

The recommended way to register an event is to use the `addEventListener` method on the target of the event:

```
  const launchButton = document.querySelector('.launch-button');
  launchButton.addEventListener('click', () => {
    alert('3!');
    alert('2!');
    alert('1!');
    alert('BLASTOFF! 💥 🚀 🌖');
  });
```

In this case, `'click'` is the name of the event. There are many other events that you can bind handlers to instead:

* `focus` -> A form field is focused, to allow the user to start typing or whatever
* `blur` -> A form field loses focus, so the user isn't able to type into it anymore
* `submit` -> A form is submitted
* `mouseenter`/`mouseout` -> The mouse enters or leaves a particular element
* `copy`/`cut`/`paste` -> The user has copied, cut, or pasted some text

And there are also other, less common events that don't involve user input: Something has started or completed loading, an animation has stopped, paused, or completed, or a websocket has opened, received data, or closed.

[This page](https://developer.mozilla.org/en-US/docs/Web/Events) outlines all of the events that the DOM makes available to bind handlers to.

### 05 - Vampire Editor

* Use the provided `findVampire` method to hard-code adding an offspring to one of the vampires
* It fails; why?
* Next create a modal: Input, Create, Cancel
  * It opens when you click a Vampire

### jQuery
* High level - What is jQuery?
* Why jQuery became popular
* Including jQuery in a project
  * CDNs - https://releases.jquery.com/
* The `jQuery()` function
* `$` What's this?
* `$(() => {});` What's this?
  * `$(document).ready(() => {})` vs. `$(() => {})`

* Using jQuery in the console
* How do you do stuff to HTML elements with jQuery? (same stuff as above)
* `$('li')` vs. `$('<li>')`
* DOM nodes vs. jQuery objects
* How do you use the jQuery docs?
* Vanilla JS vs. jQuery (Why you might not need jQuery) https://github.com/nefe/You-Dont-Need-jQuery
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
