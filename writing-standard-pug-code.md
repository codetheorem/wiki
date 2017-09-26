## Rules for writing Pug for EOS:

#### disallowAttributeConcatenation : null

Pug must not contain any attribute concatenation.
```
** If true **

//- Invalid 
a(href='text ' + title) Link 

//- Invalid under `'aggressive'`  
a(href=text + title) Link 
a(href=num1 + num2) Link

```


<br>
## Class

#### disallowClassLiterals : null

Pug must not contain any class literals.
```
** If true **

//- Invalid 
.class 

//- Valid 
div(class='class')

```
<br>
#### disallowClassLiteralsBeforeAttributes : null

All attribute blocks must be written before any class literals.

```
** If true **

//- Invalid 
input.class(type='text')  

//- Valid 
input(type='text').class

```
<br>
#### requireClassLiteralsBeforeAttributes: true

All class literals must be written before any attribute blocks.

```
//- Invalid 
input(type='text').class  

//- Valid 
input.class(type='text')

```
<br>
#### requireClassLiteralsBeforeIdLiterals: true

All class literals must be written after any ID literals.

```
//- Invalid 
input#id.class(type='text')

//- Valid 
input.class#id(type='text')

```
<br>
#### disallowClassLiteralsBeforeIdLiterals: null

All ID literals must be written before any class literals.

```
** If true **

//- Invalid 
input.class#id(type='text') 

//- Valid 
input#id.class(type='text')

```
<br>
#### disallowClassAttributeWithStaticValue: true

Prefer class literals over class attributes with static values.

```
//- Invalid 
span(class='foo')  

//- Valid 
span.foo

```

<br>
## ID

#### disallowIdAttributeWithStaticValue: true

Prefer ID literals over id attributes with static values.

```
//- Invalid 
span(id='foo')  

//- Valid 
span#id
```
<br>
#### disallowIdLiterals: null

Pug must not contain any ID literals.

```
** If true **

//- Invalid 
#id 

//- Valid 
div(id='id')
```

<br>
#### disallowIdLiteralsBeforeAttributes: null

All attribute blocks must be written before any ID literals.

```
** If true **

//- Invalid
input#id(type='text')  

//- Valid 
input(type='text')#id
```

<br>
#### requireIdLiteralsBeforeAttributes: true

All ID literals must be written before any attribute blocks.

```
//- Invalid 
input(type='text')#id  

//- Valid 
input#id(type='text')
```

<br>
#### disallowHtmlText: null

Pug must not contain any HTML text.

```
** If true **

//- Invalid 
<strong>html text</strong> 
p this is <strong>html</strong> text
```

<br>
#### disallowBlockExpansion : true

Pug must not contain any block expansion operators.

```
//- Invalid 
p: strong text 
table: tr: td text
```

<br>
#### disallowAttributeInterpolation: true

Pug must not contain any attribute interpolation operators.

```
//- Invalid 
a(href='text #{title}') Link 

//- Valid 
a(href='text \#{title}') Link 
a(href='text \\#{title}') Link
```

<br>
#### disallowDuplicateAttributes: true

Attribute blocks must not contain any duplicates. And if an ID literal is present an ID attribute must not be used. Ignores class attributes.

```
//- Invalid 
div(a='a' a='b') 
#id(id='id')  

//- Valid 
div(class='a', class='b') 
.class(class='class')
```

<br>
#### disallowMultipleLineBreaks: true

Pug must not contain multiple blank lines in a row.

```
//- Invalid 
div   


div  

//- Valid 
div  

div
```

<br>
#### disallowSpaceAfterCodeOperator: null

No code operators (-/=/!=) should be followed by any spaces.

```
** If true **

//- Invalid 
p= 'This code is <escaped>' 
p!=  'This code is <strong>not</strong> escaped'  

//- Valid 
p='This code is <escaped>' 
p!='This code is <strong>not</strong> escaped'
```

<br>
#### requireSpaceAfterCodeOperator: true

All code operators (-/=/!=) must be immediately followed by a single space.

```
//- Invalid 
p='This code is <escaped>' 
p!=  'This code is <strong>not</strong> escaped'  

//- Valid 
p= 'This code is <escaped>' 
p!= 'This code is <strong>not</strong> escaped'
```
<br>

#### disallowSpacesInsideAttributeBrackets: true

Disallows space after opening attribute bracket and before closing.

```
//- Invalid 
input( type='text' name='name' value='value' )  

//- Valid 
input(type='text' name='name' value='value')
```

<br>
#### requireSpacesInsideAttributeBrackets: null

Requires space after opening attribute bracket and before closing.

```
** If true **

//- Invalid 
input(type='text' name='name' value='value')  

//- Valid input
( type='text' name='name' value='value' )
```

<br>
#### disallowSpecificAttributes: [ { "a": "name" } ]

**e.g.:** "a" OR [ "A", "b" ]
Pug must not contain any of the attributes specified.

```
//- Invalid 
span(a='a') 
div(B='b')
```

<br>
#### disallowSpecificTags: null

Pug must not contain any of the tags specified.
**e.g.:** [ "b", "i" ]

```
//- Invalid 
b Bold text 
i Italic text
```

<br>
#### disallowStringConcatenation: true

Pug must not contain any string concatenation.

```
//- Invalid 
h1= title + 'text' 

//- Invalid under `'aggressive'` 
h1= title + text
```

<br>
#### disallowStringInterpolation: null

Pug must not contain any string interpolation operators.

** If true **

```
//- Invalid 
h1 #{title} text
```

<br>
#### disallowTagInterpolation: null

Pug must not contain any tag interpolation operators.

```
** If true **

//- Invalid 
| #[strong html] text 
p #[strong html] text
```

<br>
#### maximumNumberOfLines: null

Pug files should be at most the number of lines specified.

```
// null – no limit for maximum Number of lines
// If value is set then maximum number of lines set as per value
```

<br>
#### requireLineFeedAtFileEnd: true

All files must end with a line feed.

<br>
#### requireLowerCaseAttributes: true

All attributes must be written in lower case. Files with doctype xml are ignored.

```
//- Invalid 
div(Class='class')  

//- Valid 
div(class='class')
```

<br>
#### requireLowerCaseTags: true

All tags must be written in lower case. Files with doctype xml are ignored.

```
//- Invalid 
Div(class='class')  

//- Valid 
div(class='class')
```

<br>
#### requireSpecificAttributes:
  [ { "form": "action" }
  , { "img": "alt" }
  , { "input": "type" }
  , { "input[type=submit]": "value" }
  ]

**e.g.:** img tags must contain all of the attributes specified.

```
//- Invalid 
img(src='src')  

//- Valid 
img(src='src' alt='alt')
```

<br>
#### requireStrictEqualityOperators: true

Requires the use of === and !== instead of == and !=.

```
//- Invalid 
if true == false 
if true != false  

//- Valid 
if true === false 
if true !== false
```

<br>
#### validateAttributeQuoteMarks: "'"

**e.g.:** "'"
All attribute values must be enclosed in single quotes.

```
//- Invalid 
input(type="text" name="name" value="value")  

//- Valid 
input(type='text' name='name' value='value')
```

<br>
#### validateAttributeSeparator:
  { "separator": ", "
  , "multiLineSeparator": "\n  "
  }

**e.g.:** { "separator": ", ", "multiLineSeparator": "\n " }

- All attributes must be immediately followed by a comma and then a space.
- All attributes that are on different lines must be preceded by two spaces.

```
//- Invalid 
input(type='text' name='name' value='value') 
div   
  input(type='text'   
  , name='name'   
  , value='value'
  )  

//- Valid input(type='text', name='name', value='value') 
div   
  input(type='text'   
    name='name'   
    value='value' 
  )
```






































