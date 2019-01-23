Our CI is configured to test JS code following the Standard JS Code style defined at:
https://standardjs.com/rules.html

And, because we follow the standards, we get to put this badge in our wiki:

[![JavaScript Style Guide](https://cdn.rawgit.com/standard/standard/master/badge.svg)](https://github.com/standard/standard)

#### Don't create HTML elements inside javascript 
It is good practice to keep your javascript code and html tags separated. It makes it more easy to maintain, debug and reusable. 

Instead of creating HTML element inside javascript, create it in HTML page and update it with javascript.

```html
/* Good - ordered */

$("button").click(function(){
    var tagTemplate = $('.js-tags').text(tagName)
});

/* Bad */

 $("button").click(function(){
    tag = '<span class="label label-default">' + tagName + '</span>'
    $('.js-tags').html(jQuery.parseHTML(tag))
 });

```