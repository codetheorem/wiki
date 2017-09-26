## Rules for writing Pug for EOS:

#### disallowAttributeConcatenation : null

Pug must not contain any attribute concatenation.
```
**If true **

/* Invalid */
a(href='text ' + title) Link 

/* Invalid under `'aggressive'`  */
a(href=text + title) Link 
a(href=num1 + num2) Link

```
## Classes
-----------------------------------------------------------------------------

#### disallowClassLiterals : null

Pug must not contain any class literals.
```
**If true **

/* Invalid */
.class 

/* Valid */
div(class='class')

```