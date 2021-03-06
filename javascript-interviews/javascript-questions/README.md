<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Naming conventions](#naming-conventions)
- [JS code can be invoked in HTML in 3 ways](#js-code-can-be-invoked-in-html-in-3-ways)
- [Javascript is loosly typed, dinamically typed](#javascript-is-loosly-typed-dinamically-typed)
- [typeof() operator](#typeof-operator)
- [Hoisting](#hoisting)
- [Context (`this` keyword)](#context-this-keyword)
- [Scope](#scope)
- [Closure](#closure)
- [Map & filter](#map--filter)
- [Let & var](#let--var)
- [Promises vs Observables](#promises-vs-observables)
- [Difference between == & ===](#difference-between---)
- [Data types in JS](#data-types-in-js)
- [call / bind / apply - set custom vals for `this` ( = alter the execution context)](#call--bind--apply---set-custom-vals-for-this---alter-the-execution-context)
- [What represents the `arguments`  object](#what-represents-the-arguments--object)
- [What is a callback](#what-is-a-callback)
- [Built-in methods](#built-in-methods)
- [Differences between your framework and others](#differences-between-your-framework-and-others)
- [What makes JavaScript special (different) compared with other programming languages?](#what-makes-javascript-special-different-compared-with-other-programming-languages)
- [arrow functions](#arrow-functions)
- [What is difference between pass by value and pass by reference?](#what-is-difference-between-pass-by-value-and-pass-by-reference)
- [Unit testing](#unit-testing)
- [Testing: unit, acceptance, integration](#testing-unit-acceptance-integration)
- [Position: static = default](#position-static--default)
- [Position relative vs absolute](#position-relative-vs-absolute)
- [Z-index](#z-index)
- [Class vs ID](#class-vs-id)
- [If there are two classes for the same element, with different properties, which one is applied?](#if-there-are-two-classes-for-the-same-element-with-different-properties-which-one-is-applied)
- [CSS Specificity](#css-specificity)
- [Two way bindings vs one way](#two-way-bindings-vs-one-way)
- [Have you used any code quality tools](#have-you-used-any-code-quality-tools)
- [Anonymous functions](#anonymous-functions)
- [Why whould you use a framework for development](#why-whould-you-use-a-framework-for-development)
- [Immutability  how to implement it in your code](#immutability--how-to-implement-it-in-your-code)
- [Difference between forEach and map](#difference-between-foreach-and-map)
- [Ternary operator  what it does and syntax](#ternary-operator--what-it-does-and-syntax)
- [What css preprocessors do you know and why they are useful](#what-css-preprocessors-do-you-know-and-why-they-are-useful)
- [How do you add a click listener in vanilla Js or jQuery?](#how-do-you-add-a-click-listener-in-vanilla-js-or-jquery)
- [What are different ways HTML elements can be accessed in JS code?](#what-are-different-ways-html-elements-can-be-accessed-in-js-code)
- [What is the difference between pseudo elements and pseudoclasses](#what-is-the-difference-between-pseudo-elements-and-pseudoclasses)
- [What is the css box model?](#what-is-the-css-box-model)
- [What is the difference between undeclared and undefined](#what-is-the-difference-between-undeclared-and-undefined)
- [What is the difference between null and undefined](#what-is-the-difference-between-null-and-undefined)
- [What is the difference between LocalStorage and SessionStorage](#what-is-the-difference-between-localstorage-and-sessionstorage)
- [HTML 5 semantic tags benefits](#html-5-semantic-tags-benefits)
- [HTML 5 APIs used:](#html-5-apis-used)
- [How to create responsive css pages](#how-to-create-responsive-css-pages)
- [How to create responsive css pages without any css framework](#how-to-create-responsive-css-pages-without-any-css-framework)
- [Place an element at center of page:](#place-an-element-at-center-of-page)
- [How to hide an element on page](#how-to-hide-an-element-on-page)
- [CSS preprocessor](#css-preprocessor)
- [CSS encapsulation](#css-encapsulation)
- [How to create a new array/object from existent array/object](#how-to-create-a-new-arrayobject-from-existent-arrayobject)
- [Imediatlly Invokable Function Expression - and How to use IIFE scoped vars globally](#imediatlly-invokable-function-expression---and-how-to-use-iife-scoped-vars-globally)
- [let vs var](#let-vs-var)
- [CORS - Cross Origin Resouce Sharing](#cors---cross-origin-resouce-sharing)
- [What is `this` object?](#what-is-this-object)
- [How to change `this`? -](#how-to-change-this--)
- [Arrow functions - arrow functions](#arrow-functions---arrow-functions)
- [Security principles cookies, local storage](#security-principles-cookies-local-storage)
- [foreach vs map](#foreach-vs-map)
- [Angular Interview Questions (outside this repo)](#angular-interview-questions-outside-this-repo)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# Naming conventions

- cannot use reserved keywords for vars
- vars should not start with a numeral
- vars in JS are case sensitive

# JS code can be invoked in HTML in 3 ways
- inline (inside HTML element: `<button type="button" onclick="documet.getElementById('tt)'.innerHTML='Just mess around'">Try it</button>`)
- external (include the script providing the src file reference)
- internal (JS code inside `<script> tag`)

# Javascript is loosly typed, dinamically typed

Unlike other languages, Javascript is loosly typed, dinamically typed - a variable can hold multiple types (eg number and string);
TypeScript is strongly typed =  staticaly typed

# typeof() operator

The typeof(operand), applied to the operand variable, returns the thype of that variable

#  Hoisting

- is about allocation of memory for each var, no matter the place where vars are declared. Should declare vars at the begin of file/scope; 
- use strict so that you'll get an error if you miss variable declaration before using it

# Context (`this` keyword)
 
 - CONTEXT refers to the object to which a function belongs; `this` object, basically, is the environment. Global environment = Global execution CONTEXT.
 - In global scope `this` represents the window object;
 - Inside an inner fc/context `this` is `the object on which the event that triggerd the function happened` = is bound to the event handler referencing the DOM elem: `` myLink -> $( myLink ).on( click , myFc)``; - vars declared without keyword are global - bad practice  do not clutter the global object.

# Scope
- Is about the visibility of the variable
- There are two scopes: local and global;
Using `let`  keyword to declare the variables, the scope( the place where those variables are visible) becomes the nearest block (e.g an if block statement), using `var`, those vars will be visible inside the function where they were declared;

#  Closure 

The inner function can access the variables of the enclosing function due to closures in JavaScript. In other words, the inner function preserves the scope chain of the enclosing function at the time the enclosing function was executed, and thus can access the enclosing function's variables.  Normally, when a function finishes execution,  it's vars cease to exist, but not in this case (scope chain).

```JavaScript
function outer() {
var b = 10;
   function inner() {
        
         var a = 20; 
         console.log(a+b);
    }
   return inner;
}
var X = outer(); 
console.dir(X);
```
A closure gives us access to an outer function's scope from an inner function. 
![context+scope](./../context+scope.jpeg)

#  Map & filter

#  Let & var 
- Let keyword declares a var available only for that fc/block of declaration, var declares for the entire function/file

#  Promises vs Observables

A promise is an object that may produce a single value some time in the future: either a resolved value, or a reason that it’s not resolved (e.g., a network error occurred). A promise may be in one of 3 possible states: 
- Fulfilled: onFulfilled() will be called (e.g., resolve() was called)
- Rejected: onRejected() will be called (e.g., reject() was called)
- Pending: not yet fulfilled or rejected.

Promise users can attach callbacks(a Promise gets as params 2 functions) to handle the fulfilled value or the reason for rejection.
Promises are an esier way then callbacks to solve asynchronos code execution. Instead of using callbacks functions we return a `new Promise(resolve, reject)` object.
In order to use the promise we call the function and chain the then and catch methods. The then  is going to be our success callback and catch our fails callback.

```JavaScript
 function myPromiseFc() {
  //  the construtor of a promise receives as parameters two callback functions
   return new Promise(resolve, reject) { 
     if (0 == 0) {
       resolve('resolved info')
     } else {
       reject('reject info')
     }
   }
 }

 // And of course in order to use the promise we call the function and chain the then and catch methods

 myPromiseFc().then(msg => console.log(msg)).catch(err => console.log(err.message));
```
Promises solve the callback hell problem (when we need multiple callbacks): insted of nesting a callback inside a callback inside a callback, just chain `.then()` methods one after the other.
Promises are eager, meaning that a promise will start doing whatever task you give it as soon as the promise constructor is invoked.
They return all the result at once ( compared to the Observable streams of data - nothing happens until a subscription has been made to that stream of data, or with tasks - which are lazy).

We use `Promise.all([promise1, promise2, promise3]).then(messages){console.log(messages)}` method to get the responses after all promises passed as params are completed. The benefit is that all promisses start executing in the same time, and if one promise is slow (e.g. gets some data from the server, the following promises do not wait for it to finish execution)
If we run ``Promise.race([promise1, promise2, promise3]).then(message){console.log(message)}`` it will return a soon as the first promise is completed.

#  Difference between == & === 
- used to check value  equality (compare variable's values) 
- === is strict equality - used to compare the val and type of variables
# Data types in JS
- primitives: number, boolean, string, undefined,null - is a primitive, though typeof(null)=object - a bug in JS
- objects(arrays,functions,obj,null)

# call / bind / apply - set custom vals for `this` ( = alter the execution context)

- All three functions(call, bind, apply) can be used to set values for `this` object.
- The apply() method calls a function with a given `this` value, and arguments provided as an array (or an array-like object).
- bind() creates a new function, from the initial one, where the value of `this` is the value provided as param: ``  const bindedFc= unbindedFc.bind(param)``
# What represents the `arguments`  object

- inside a function, `arguments` are the args of that function, as an array, with first element starting at position 0
# What is a callback

The callback is a function that has to be executed after another function has finished executing;
This callback function is provided as an argument to another function, in order to be executed as a callback.

# Built-in methods

- string.charAt
- string.concat
- array.forEach(fc) - calls a function on each on each element in the array
- string.indexOf(searched) - applied on a string, returns the index of the position the seached string passed as param is encountered in the string
- length - returns the length
- array.pop - removes the last elem from array and returns this elem
- array.push - adds one or more elems to the end of the array and returns the length of that array
- array.reverse() - reverses the order of the elements in the array


# Differences between your framework and others 

Well, I could say that my favorite framework is Angular, because the most complex UIs I developed were in Angular.
Unlike React or Vue, Angular comes with a complex CLI, has all the packages (including the router - out of the box), provides implementations for lazy loading pattern with RxJs and ngRx for REDUX pattern implementation. Also security plementation seems to me more rich in libraries for implementing protocols like OpenID Connect, Oauth, Auth 2.

Compared to it, React doesn't provide files with clear implementation of the MVC pattern.

# What makes JavaScript special (different) compared with other programming languages?
- scope global vs local  scope chain
- code is executed at runtime (thus is used on Client side - executed in browser)
- execution stack and event queue
- I would also mention the event loop. The way JS handles more than one tasks as a time. Thoungh JS is single-threaded, executes code synchronously, there is a way to handle async events with the help of the browser APIs. Js puts all the tasks to exe in the execution stack. When it has somethig to execute after a wile, a time interval, will notify a WebApi that sets a timer and takes care to push into the event queue the task, at the exact right time. After the exe stack is emptied, JS checks in the event que for tasks to executecute, and executes each tasks from event que, each time the stack is empty.
- other languages (CSS, HTML, PUG, JADE, Java can be transpiled into JavaScript)

![exe-stack](./../exe-stack-event-que.jpg)

- Js is compiled at runtime, runs mainly in browser but also on server,cross compilers convert different lang in Js and Java, 
- native query capabilities are available only through libs like underscore.js

# arrow functions 
 - short notation for anonymous functions,  the `=>` means return). An arrow function expression is similar to what in other programming languages is known as lambda functions
 - a great aspect is that the arrow function alredy binds the `this` keyword from inside the function to the context object where the arrow function is placed; thus if function is declare inside a component, `this` will be the context of that component;
 
#  What is difference between pass by value and pass by reference? 
Js always calls functions by directly  passing params values, not the address of variables. However, when the variable refers to an object which includes array, the value is the reference to the object  not basically the address of the object, but copy of the object.

# Unit testing 
Frameworks: MockaJs, AVA, Jest, Jasmine, Karma(the test runner engine), Cypress 

# Testing: unit, acceptance, integration

# Position: static = default

- z-index does not work with position-static;

# Position relative vs absolute

`position relative` means relative to itself = position elements one after the other and shift elements by specified top, left, bottom and right values from where the element would normally be; After setting position to relative z-index is enabled, and if not specified will set the layer of element the top layer; 
`position: fixed` means positioned relative to the viewport, or the browser window itself.
 The viewport doesn't change when the window is scrolled, so a fixed positioned element will stay right where it is when the page is scrolled(to fix buttons under this element use CSS  scroll-margin-top: 5rem; /* whatever is a nice number that gets you past the header */
`position: sticky` for an element means the element will just sit there like a static element, but as you scroll past it, if it's parent element has room (usually: extra height) the sticky element will behave as if it's fixed until that parent element is out of room. ;

`position: absolute` is used in order to place any page elem exactly where you want it; specify `top`, `left`, `right`, `bottom` relative to the immediately outer parent element with absolute  if there is none, pos will be relative to the html page.
 - elements assigned the `position: absolute` property, are removed from the flow of elements on the page, thus don't over use it;

# Z-index 

`z-index: ` is an integer value representing the number of the view layer;
- closest layer to the viewer has the greater value and is the most visible
 
#  Class vs ID 
We use . for class selectors, wich are not unique in an HTML element
We use # for HTML elements IDs wich are unique in HTML pages

#  If there are two classes for the same element, with different properties, which one is applied?

-  the one with higher specificity 
-  the one with the more specific rule,
-  the one with the last rule defined,
-  the one with the embeded CSS,
- class selector beats element selector;

#  CSS Specificity 
- for body specificity is 0,0,0,0
 Specificity ierarhy: 
 - inline style(specificity 1000) > IDs( specificity 100)>class selector and pseudoclass selectors(specificity 10) beats>elements(p has specificity 1) & pseudoelements selectors (:before has specificity 10)

# Two way bindings vs one way 
 - from template to js via input, from js to template  in React by default -2 waydata binding, in Angular  use [(ngModel)], in Vue `v-model`

# Have you used any code quality tools 
 - I use Linters (JSLint, TSLint)

# Anonymous functions 

Function literal, lambda abstraction, or lambda expression is a function definition that is not bound to an identifier ( doesn't have a name). Anonymous functions are often arguments being passed to higher-order functions, or used for constructing the result of a higher-order function that needs to return a function. If the function is only used once, or a limited number of times, an anonymous function may be syntactically lighter than using a named function. Anonymous functions are ubiquitous in functional programming languages and other languages with first-class functions( passsed as param to map, filter, sort, reduce, includes, some, every, find), where they fulfill the same role for the function type as literals do for other data types.

# Why whould you use a framework for development

I use frameworks for the abstraction they offer.
Frameworks do all of the heavy lifting for us so that we can concentrate on building great products. 
Good implementation of design patterns starting with MVC, Lazy loading, Singleton, Factory, Observer, Redux (Redux is not for every implementaion but it has it's benefits).
Frameworks promote and ease the develpment following good practices, provide easy setup running configuration files, CLIs, wich are great.

# Immutability  how to implement it in your code  
- do not mutate array, preferably do not use foreach but rather use map, filter- all the functions should return a value (not void type) and shoud not change global variables; alternative: use immutable.js or Mori libs.
# Difference between forEach and map
- one mutates the array : forEach receives as param a fc. and applies that fc. for each elem  of the array and  does not return anything;
- map does not mutate the array, but creates a new array using the function passed as argument and  returns that new array
# Ternary operator  what it does and syntax 
- short if statement: cond ? onTrue : onFalse
# What css preprocessors do you know and why they are useful
- SASS,LESS  write css in a cleaner manner

# How do you add a click listener in vanilla Js or jQuery? 
$( #myElem ).on( click , functionToExe);

# What are different ways HTML elements can be accessed in JS code?

```JavaScript
document.getElementById('idvalue');
document.getElementsByClassName('className');
document.getElementByTagName('p');
document.querySelector('p.myParagraphName > div'); 
// gets as param a CSS style selector and returns the first occurence of the element
//  that maches the query
```

# What is the difference between pseudo elements and pseudoclasses 
Pseudo-classes = fake classes, have the benefit that they select regular elements but under certain conditions(not all the time), like when their position relative to siblings or when they are under a particular state, dynamic :link, :visited, :hover, :active,:focus, :first-child, :nth-child(n) , :nth-last-child(n), :nth-of-type(n),:nth-last-of-type(n), :last-child, :first-of-type, :last-of-type, :only-child, :only-of-type, :root, :empty
Other pseudo-classes:  :not(x), :target, :lang(language)
Pseudo-elements = fake elements, effectively create new elements that are not specified in the mark-up of the document and can be manipulated much like a regular element. The  benefit is that they allow to create cool effects with minimal mark-up (::before, ::after, ::first-letter, ::first-line)

# What is the css box model? 
 each HTML element is wrapped inside a box(has: margin-border-pading-width+height)  can visualize it in Firebug. Use CSS reset (framework or custom CSS reset) in order to remove default browser stylings(default padding and margin of elements).

# What is the difference between undeclared and undefined

- `undefined` is a primitive;
- `undefined` is a property of the global object
- variables are of type `undefined` if they were declared but not initialized
- undeclared are those variables that are not declared (with var, let, const or without keyword - bad practice - those declare without keyword will have a global scope - clutter the `window` object)

# What is the difference between null and undefined

 We can use `null` to initialize variables, thought typeof(null)  returns object (this is a bug in JS), `null` is a primitive, and thus we can use it to initialize vars of type number, boolean, string;

`undefined` is a primitive in Javascript. `undefined` is a property of the global object. Do not use it tu initialize variables!
A variable has the value undefined if it was not initialized. A function has the value undefined if does not return a value
 typeof(undefined) is undefined. To determine whether a variable has a value use strict comparison ``typeof(variable) === 'undefined'``
 
  # What is the difference between LocalStorage and SessionStorage

  Both LocalStorage and SessionStorage store data on client side;
  LocalStorage data stays until is manually cleared through settings or explicitlly  through program
  Session Storage gets cleared when you close the browser

# HTML 5 semantic tags benefits
- simplify the work for browsers, search engines and developers (header, nav, section, article, aside, footer)
media (video and audio elements) - these come with different JS methods(play, pause, load);

# HTML 5 APIs used:
- media (video and audio elements) - these come with different JS methods(play, pause, load);
- text track API (subtitles, captions, chapters, metadata)
- drag and drop API - brings native drag and drop support to the browser
- Offline - Application Cache API - creates a manifest used by the user browser to keep a copy of the files loded by the site, in the browser
- User Interaction - use contenteditable combine with local storage to track changes to documents
- History, Canvas 2D, Web Storage, Web Sokets - alows page to send 2 way messages between server and browser
- Local Storage - HTML Web Storage API - more secure than cookies and large amounts of data can be stored,
- SSE - Server Sent Events - updates from server to the web page come automatically

# How to create responsive css pages 
- We can do it either using frameworks like: bootstrap, material, ant or using CSS grid layout

# How to create responsive css pages without any css framework

We make use of the powerfull, 2 dimentional CSS grid layout available, supported by most browsers. We combine it with flexbox display and media-queries styles. We can also test using the breaking points offered by google Chrome inspector, but is better to also test on different divices, different browsers (Windows, MacOs, Android, iOS). We have grid: container, items, cells, traks(rows or columns), areas;

The Most Powerful Lines in Grid is fluid width columns that break into more or less columns as space is available, with no media queries!

```CSS
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  /* This is better for small screens, once min() is better supported */
  /* grid-template-columns: repeat(auto-fill, minmax(min(200px, 100%), 1fr)); */
  grid-gap: 1rem;
  /* This is the standardized property now, but has slightly less support */
  /* gap: 1rem */
}
```
- [https://css-tricks.com/snippets/css/complete-guide-grid/](https://css-tricks.com/snippets/css/complete-guide-grid/)

- [NgConf CSS grid on youtube - todo - use the repo from Git](https://www.youtube.com/watch?v=lh6n0JxXD_g)
# Place an element at center of page:

Use transform: translate with position:fixed:
```CSS
.centered {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%); 
  // because the translate value from transform is based on the dimention of the element we want to center 
}
```
OR use flexbox:
```CSS
.box {
  display: flex;
  align-items: center;
  justify-content: center;
}

.box div {
  width: 100px;
  height: 100px;
}
```
# How to hide an element on page 
 - is better to use `display: none` than hidden attribute; hidden keeps the element in the DOM (element takes space)
# CSS preprocessor 
 LESS, SASS - help in CSS writing, SASS has if/then/else statements, for loops, while loops, and each loops, @extend (extend another class - basicaly copies the code from another CSS class into that class that extends it), @include and different mixins that help to write succint and inteligile code-  for example:

```CSS
.bam {
  @include background(
    image-url("foo.png"),
    linear-gradient(top left, #333, #0c0),
    radial-gradient(#c00, #fff 100px)
  );
}
```
this transpliled turns into the CSS that provide the gradient background required for all browsers:

```CSS
.bam {
  background: url('/foo.png'), -webkit-gradient(linear, 0% 0%, 100% 100%, color-stop(0%, #333333), color-stop(100%, #00cc00)), -webkit-gradient(radial, 50% 50%, 0, 50% 50%, 100, color-stop(0%, #cc0000), color-stop(100%, #ffffff));
  background: url('/foo.png'), -webkit-linear-gradient(top left, #333333, #00cc00), -webkit-radial-gradient(#cc0000, #ffffff 100px);
  background: url('/foo.png'), -moz-linear-gradient(top left, #333333, #00cc00), -moz-radial-gradient(#cc0000, #ffffff 100px);
  background: url('/foo.png'), -o-linear-gradient(top left, #333333, #00cc00), -o-radial-gradient(#cc0000, #ffffff 100px);
  background: url('/foo.png'), -ms-linear-gradient(top left, #333333, #00cc00), -ms-radial-gradient(#cc0000, #ffffff 100px);
  background: url('/foo.png'), linear-gradient(top left, #333333, #00cc00), radial-gradient(#cc0000, #ffffff 100px);
}
```
# CSS encapsulation

The styles specified within the `@Component` metadata, apply only inside that component. They are not inherited by any component. We can manipulate the view encapsulation seting the encapsulation in metadata:

```TypeScript
 encapsulation: ViewEncapsulation.None // don't provide any template or style encapsulation

 // use style array or styleURLs array
 ```
# How to create a new array/object from existent array/object

I have tried using ``splice()`` or ``{...oldObj}``(spread operator), however for multiple levels object/arrays, in order not to mutate the initial object, the safe way is: 
```JavaScript
let newObj = JSON.parse(JSON.stringify(initalObj)); // transform object into string(which is unmmutable) and backto object
```
# Imediatlly Invokable Function Expression - and How to use IIFE scoped vars globally 
- without `use strict` mode, you can declare variables without the `var` or `let` keywords, thus those variables will be global - on the global object (Window) - but it is a bad practice to cluter global object

# let vs var

Variables declared with `let` are not hoisted (allocated memorie on top of the file) because they are visible only inside their declaration block (not outside - they have a local scope);
Variables declared with `var` are visible inside the block/function where they where declared, and also in the enclosing function (in the outer function of their declaration - this si the closure - scope chain)

# CORS - Cross Origin Resouce Sharing 
- is a standard used to allow some cross origin requests, while rejecting others. In sites that offer embeded services we might have to relax some certain restriction, or else we will encouter: CORS error -  the same origin policy disallows reading from remote resource;

# What is `this` object? 
= the CONTEXT, the environment
- inside a function that is the value of a property for an object `ownerObject`, the `this` keyword represents the `ownerObject` object;

# How to change `this`? - 
By the means of:
call / bind / apply - set custom vals for this ( = alter the execution context)
All three functions(call, bind, apply) can be used to set values for `this` object.
The `apply()` method calls a function with a given `this` value, and arguments provided as an array (or an array-like object).
`bind()` creates a new function, from the initial one, where the value of `this` is the value provided as param: const bindedFc= unbindedFc.bind(param)

# Arrow functions - arrow functions
- short notation for anonymous functions, (the `=>` means return). An arrow function expression is similar to what in other programming languages is known as lambda functions;
- a great aspect is that the arrow function alredy binds the `this` keyword from inside the function to the context object where the arrow function is placed; thus if function is declare inside a component, this will be the context of that component;

# Security principles cookies, local storage 
- Angular is great when it comes to security. Helps with XSS, XSRF, sanitizing inputs. Cookies introduce vulnerabilitie,Nowdays to prevent XSRF, by using web tokens and identity servers we can have secure implementations - like the Single Sign On experience, implementations  of OIDC protocol, OAuth 2;
We can also use less cookies and instead use web tokens, local storage;
We have to pay attention not to send any sensitive date in the router params or in JSON payloads among APIs requests.

# foreach vs map

both are applied to an array and receive a callback fc. as param; `forEach` mutates the array, by alling the callback on each elem of the array; map, does not mutate the array, it returns a new array from the initial array, by apping the function receveide as param, to each element from the initial array
 # Angular Interview Questions (outside this repo)

 [https://github.com/bitaemi/Angular-ngRx-Jest-Marble/blob/angular-unit-tests-jest-marble/src/app/angular-readme/README.md#angular-interview-questions](https://github.com/bitaemi/Angular-ngRx-Jest-Marble/blob/angular-unit-tests-jest-marble/src/app/angular-readme/README.md#angular-interview-questions)