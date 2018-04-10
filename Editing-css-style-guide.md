The main principle behind EOS theme is: never modify Bootstrap vendor files, but overwrite it in a smart way to make it reusable across the product and sub-products.

We use most of OOCSS standards and have created our own rules as well in order to have a flexible codebase that can live in harmony with Bootstrap classes, variables and mixins.

## Rules for writing CSS for EOS:

#### Override Bootstrap
Before creating any new class or component, make sure Bootstrap doesn't have a component already, that even looking differently, behaves the same way and by overriding its style you can accomplish the same result.
Also, make sure the component you are overriding isn't being used in other sections in EOS and you will not break it by overriding variables or classes.
In any case, consistency is always preferred, so if the component is being used, it is recommended to align both to look and behave the same way.

#### Class Names

Class names should be __lowercase with each word separated by a dash__. Although OOCSS recommends using camel case, for consistency reasons with Bootstrap classes, we use it this same way.

```scss
/* Good - use dashes and lower case */

.this-is-good {}

/* Bad - don't use underscores */

.this_is_bad {}

/* Bad - don't use upper case */

.THIS-IS-BAD {}

/* Bad - don't use camel case */

.thisIsBad {}
```

#### Declaration order
Ordering properties within a class should consider __alphabetical order__. Even when ordering by type makes more sense, ordering alphabetically takes far less time for non-frequent CSS contributor learning where to place a certain property, as well as when a new property appears in the market the team should have to update the rules for its ordering.
On the other hand, there are plugins for IDEs to order properties alphabetically, which also makes coding faster.
For regular contributors, alphabetical ordering makes it easier to avoid duplicating properties in a class.

```scss
/* Good - ordered */

.this-is-good {
  background: #ccc;
  font-size: 14px;
  height: 100px;
  width: 50px;
}

/* Bad */

.this_is_bad {
  background: #ccc;
  height: 100px;
  width: 50px;
  font-size: 14px;
}
```

#### Indentation

Each indentation level is made up of __two spaces__. Do not use tabs. 
(Please set your editor to use two spaces)


```scss
/* Good */

.stubbornella {
  color: #fff;
  background-color: #000;
}

/* Bad - all on one line */

.stubbornella {color: #fff; background-color: #000;}

/* Bad - more than 2 spaces */

.stubbornella {
    color: #fff; 
    background-color: #000;
}

```

Rules inside of @media must be indented an additional level.

```scss
/* Good */

@media screen and (max-width:480px) {

  .stubbornella {
    color: green;
  }
}
```

#### Brace Alignment

The opening brace should be on the same line as the last selector in the rule and should be preceded by a space. The closing brace should be on its own line after the last property and be indented to the same level as the line on which the opening brace is.

```scss
/* Good */

.stubbornella {
  color: #fff;
}

/* Bad - closing brace is in the wrong place */

.stubbornella {
  color: #fff;
  }

/* Bad - opening brace missing space */

.stubbornella{
  color: #fff;
}

```


#### Property Format

Each property must be on its own line and indented one level. There should be no space before the colon and one space after. All properties must end with a semicolon.

```scss
/* Good */

.stubbornella {
  background-color: blue;
  color: red;
}

/* Bad - missing spaces after colons */

.stubbornella {
  background-color:blue;
  color:red;
}

/* Bad - missing last semicolon */

.stubbornella {
  background-color: blue;
  color:red
}
```

#### No ID selectors

While it is possible to select elements by ID in CSS, it should generally be considered an anti-pattern. ID selectors introduce an unnecessarily high level of specificity to your rule declarations, and they are not reusable.

#### JavaScript hooks

Avoid binding to the same class in both your CSS and JavaScript. Conflating the two often leads to, at a minimum, time wasted during refactoring when a developer must cross-reference each class they are changing, and at its worst, developers being afraid to make changes for fear of breaking functionality.
Create JavaScript-specific classes to bind to, prefixed with **.js-**


```html
<!-- Good - .js-btn-send-activation has no properties in CSS -->

<div class='btn btn-default js-btn-send-activation'></div>

<script>
  $('.js-btn-send-activation').on('click', ...)
</script>

<!-- Bad -->

<div class='btn-send-activation'></div>

<style>
.btn-send-activation {
  .btn;
  .btn-default;
}
</style>

<script>
  $('.btn-send-activation').on('click', ...)
</script>

````

<a name="css-preprocessors"></a>
#### Using CSS Preprocessors

Keep nesting to 3 levels deep. Always have an empty line when a new class starts and ends

```scss
/* Good */

.stubbornella {
  ...

  .inner {
    ...

    .title {
      ....

      .subtxt {
        ...
      }
    }
  }
}

/* Bad - more than 3 levels of nesting and no empty line */

.stubbornella {
  .inner {
    ...
    .title {
      ....
      .subtxt {
        ...
        .element {
          ...
        }
      }
    }
  }
}

```

**Nested selectors**

Nested selectors, if necessary, go last, and nothing goes after them. Add whitespace between your rule declarations and nested selectors, as well as between adjacent nested selectors. Apply the same guidelines as above to your nested selectors.

```scss
/* Good */

.btn-default {
  background: @btn-default-bg;
  font-weight: bold;
  @include transition(background 0.5s ease);

  .icon {
    margin-right: @space-xs;
  }
}

/* Bad */

.btn-default {
  background: @btn-default-bg;
  @include transition(background 0.5s ease);

  .icon {
    margin-right: @space-xs;
  }
  
  font-weight: bold;
  font-size: 14px;
}

```

**@extend and @include (SASS) / mixins (LESS)**
Declare @extend followed by @include statements first in a declaration block.

```scss
/* Good */

.stubbornella {
  @extend .company;
  @include border-rounded(14px);
  color: @stubbornella-color;
  font-style: underline;
}

/* Bad */

.stubbornella {
  color: @stubbornella-color;
  @extend .company;
  font-style: underline;
  @include border-rounded(14px);
}
```

**Global variables: hex colors, pixels, fonts, etc.**
The variables that control all other variables in the document. They don't need to be specific to a class or component, but rather global enough to be applied to other variables.
Consider using the name of the property, element type, status type, and always add at the end **-base**.
Consider overwriting Bootstrap classes when possible.

```scss
/* Good */

@font-size-base: 13px;
@font-color-base: #ccc;
@bg-color-base: #ccc;
@danger-color-base: #de1a1a;
@primary-color-base: #6bbf59;
@h1-font-size-base: 33px;

/* Good usage of global variables */

@panel-title-size: @h1-font-size-base;

/* Bad - the font-size of any specific element should come from a -base variable */

@panel-title-size: 33px;

/* Bad - no -base added */

@body-bg-color: #ccc;

/* Bad - use a base variable for the font family as well */

@font-family-panel: "Lato";

/* Good */

@font-family-serif-base: "Roboto";
@font-family-sans-serif-base: "Lato";
@font-family-base: @font-family-sans-serif-base;
```


**Specific variables**
The variables to be used inside a property class.
Name variables after the class/element, followed by its status, and adding at the end the property it modifies.

```scss
/* Good */

@stubbornella-font-size: 14px;
@stubbornella-color: #ccc;

.stubbornella {
  color: @stubbornella-color;
  font-size: @stubbornella-font-size;
}

/* Bad - color should be used from a variable */

.stubbornella {
  color: #ccc;
}

/* Bad - a variable for the color in stubbornella should be first defined in the variables.scss file but never use the global variables directly */

.stubbornella {
  color: @primary-color-base;
}
```

Group the set of variables in a sensible way, according to the element/block they will modify, by using a comment at the beginning of the block:

```scss
/* Good */

//========= stubbornella ==========

@stubbornella-font-size: 14px;
@stubbornella-color: #ccc;
@stubbornella-border: 1px solid #ccc;

//========= foo ==========

@foo-bg: #898989;
@foo-font-size: @font-size-base;
@foo-margin-top: 8px;

```


#### Mixins

Use mixins inside semantic classes whenever it is possible. Avoid creating a new class just for the sake of adding a mixin inside it alone.

```scss
/* Good - Recommended */

.text-right {
  align-text: right;
  font-size: 14px;
}

.foo {
  @extend text-right; //extend is recommended when specifity allows it
  font-color: #ccc;
}

.bar {
  @include text-right;
  font-color: #555;
}
```

```html
<!-- Try to avoid -->
<div class="foo text-right">...</div>

<!-- Unless you only need the text-right class -->
<div class="text-right">...</div>

```


#### Vendor-Prefixed: auto-prefixes

Unless special case where a vendor prefix needs special value, avoid using vendor prefixes always.

```scss
/* Bad */

.foo {
  -moz-border-radius: 4px;
  -webkit-border-radius: 4px;
  border-radius: 4px;
}

/* Good */

.foo {
  border-radius: 4px;
}

```
Check [shouldiprefix.com](http://shouldiprefix.com) when you are not sure!

#### Border

Use 0 instead of none to specify that a style has no border.

```scss
/* Good */

.foo {
  border: 0;
}

/* Bad */

.foo {
  border: none;
}

```

#### Do not use units with zero values

Zero values do not require named units, omit the “px” or other units.

```scss
/* Good */

.stubbornella {
  margin: 0;
}

/* Bad - uses units */

.stubbornella {
  margin: 0px;
}
```

#### Selectors

Each selector should appear on its own line. The line should break immediately after the comma. Each selector should be aligned to the same left column.

```scss
/* Good */

button,
input.button {
  color: @button-color;
}

/* Bad - selectors on one line */

button, input.button {
  color: @button-color;
}
```

#### :hover and :focus

If :hover pseudo class is styled, :focus should also be styled for accessibility. Focus styles should never be removed.

```scss
/* Good */

a:hover,
a:focus {
  color: @link-hover-color;
}

/* Good */

a:hover {
  color: @link-hover-color;
}

a:focus {
  color: @link-focus-color;
}


/* Bad - missing :focus */

a:hover {
  color: @link-hover-color;
}
```


#### Width and height on components

No heights on anything that contains text. Components should be flexible and their widths should be controlled by grids. This will guarantee re-usable components.

```scss
/* Good - no width specified */

.callout-content {
  border: 1px solid @callout-border-color;
  background: @callout-bg;
}

/* Bad - dimension specified */

.callout-content {
  width: 200px;
  height: 150px;
  border: 1px solid @callout-border-color;
  background: @callout-bg;
}
```


#### Single quotes

Don't use double quotes in properties values

```scss
/* Good */

.callout-content {
  content: 'some text to display';
}

/* Bad */

.callout-content {
  content: "some text to display";
}
```
