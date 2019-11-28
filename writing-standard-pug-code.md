◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#writing-code)


# Rules for writing Pug for EOS:


## Class

#### requireClassLiteralsBeforeAttributes: true

All class literals must be written before any attribute blocks.

```
//- Invalid 
input(type='text').class  

//- Valid 
input.class(type='text')

```



#### disallowClassLiteralsBeforeIdLiterals: true

All ID literals must be written before any class literals.

```
//- Invalid 
input.class#id(type='text') 

//- Valid 
input#id.class(type='text')

```



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



#### requireIdLiteralsBeforeAttributes: true

All ID literals must be written before any attribute blocks.

```
//- Invalid 
input(type='text')#id  

//- Valid 
input#id(type='text')
```


#### disallowHtmlText: true

Pug must not contain any HTML text.

```
//- Invalid 
<strong>html text</strong> 
p this is <strong>html</strong> text
```



#### disallowBlockExpansion : true

Pug must not contain any block expansion operators.

```
//- Invalid 
p: strong text 
table: tr: td text
```



#### disallowAttributeInterpolation: true

Pug must not contain any attribute interpolation operators.

```
//- Invalid 
a(href='text #{title}') Link 

//- Valid 
a(href='text \#{title}') Link 
a(href='text \\#{title}') Link
```


#### disallowDuplicateAttributes: true

Attribute blocks must not contain any duplicates. And if an ID literal is present an ID attribute must not be used. Ignores class attributes.

```
//- Invalid 
div(a='a' a='b') 
#id(id='id')  

//- Valid 
.class(class='class')
```


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



#### disallowSpacesInsideAttributeBrackets: true

Disallows space after opening attribute bracket and before closing.

```
//- Invalid 
input( type='text' name='name' value='value' )  

//- Valid 
input(type='text' name='name' value='value')
```


#### requireLineFeedAtFileEnd: true

All files must end with a line feed.


#### requireLowerCaseAttributes: true

All attributes must be written in lower case. Files with doctype xml are ignored.

```
//- Invalid 
div(Class='class')  

//- Valid 
.class(class='class')
```


#### requireLowerCaseTags: true

All tags must be written in lower case. Files with doctype xml are ignored.

```
//- Invalid 
Div

//- Valid 
div
```


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


#### validateAttributeQuoteMarks: "'"

**e.g.:** "'"
All attribute values must be enclosed in single quotes.

```
//- Invalid 
input(type="text" name="name" value="value")  

//- Valid 
input(type='text' name='name' value='value')
```


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

//- Valid
input(type='text', name='name', value='value') 

div   
  input(type='text'   
    name='name'   
    value='value' 
  )
```



