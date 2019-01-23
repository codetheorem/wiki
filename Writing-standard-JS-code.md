Our CI is configured to test JS code following the Standard JS Code style defined at:
https://standardjs.com/rules.html

And, because we follow the standards, we get to put this badge in our wiki:

[![JavaScript Style Guide](https://cdn.rawgit.com/standard/standard/master/badge.svg)](https://github.com/standard/standard)

#### Do not use HTML elements in javascript  files
It is good practice to keep javascript code and html elements separated. It makes it easier to maintain and debug, and  is reusable. 

Instead of creating HTML element inside javascript, create it in an HTML page and update it with javascript.

```html
/* Good */

$("button").click(function(){
    var tagTemplate = $('.js-tags').text(tagName)
});

/* Bad */

 $("button").click(function(){
    tag = '<span class="label label-default">' + tagName + '</span>'
    $('.js-tags').html(jQuery.parseHTML(tag))
 });

```