Our CI is configured to test JS code following the Standard JS Code style defined at:
https://standardjs.com/rules.html

And, because we follow the standards, we get to put this badge in our wiki:

[![JavaScript Style Guide](https://cdn.rawgit.com/standard/standard/master/badge.svg)](https://github.com/standard/standard)
#### Calling app controller
When we need to call a controller in a specific page/section, make sure you add the `.js-` prefix plus the controller name to the first `.container` element.  
Inside our JS we use:

```js
if ($('.js-controllerName').length) {
    controllerName()
  }
```
to only call the controller when needed.

#### ES5/ES6 syntax
- Use `let` for variables that will change their value over time, and `const` for variables which cannot be reassigned.
- Always use template literals.
- Use arrow function and function expression instead of function declaration when possible (use function declaration when the scope of this is needed, ex: jQuery selectors).
- For object methods use `arrow function` syntax.
- Use Async Await for asynchronous tasks.
- Always wrap your async/await code in a `try/catch block`.
- Use `_` to define temporary variables, ex: `_data` to refer to a big object, then `data` to refer to the final (reduced) form of the object.
- Use `$` to define template variable, ex: `const $video = $('.js-video-container').clone(true)`
- Use `object destructuring` instead of variable assignment, ex: `const { name } = object` instead of `const name = object.name`. We also use a space inside brackets `{ name }`

#### Do not use HTML elements in javascript  files
It is good practice to keep javascript code and html elements separated. It makes it easier to maintain and debug, and  is reusable. 

Instead of creating HTML element inside javascript, create it in an HTML page and update it with javascript.

```html
/* Good */

$("button").click(function(){
    const $tagTemplate = $('.js-tags').text(tagName)
});

/* Bad */

 $("button").click(function(){
    tag = `<span class="label label-default">${tagName}</span>`
    $('.js-tags').html(jQuery.parseHTML(tag))
 });

```