◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#writing-code)


# Comment formatting

Well commented code is extremely important. Take time to describe components, how they work, their limitations, and the way they are constructed. Don't leave others in the team guessing as to the purpose of uncommon or non-obvious code.

Comment style should be simple and consistent within a single code base.

* Place comments on a new line above their subject.
* Keep line-length to a sensible maximum, e.g., 80 columns.
* Make liberal use of comments to break code into discrete sections.
* Use "sentence case" comments and consistent text indentation.

```
/* ==========================================================================
   Section comment block
   ========================================================================== */

/* Sub-section comment block
   ========================================================================== */

/**
 * Short description using Doxygen-style comment format
 *
 * The first sentence of the long description starts here and continues on this
 * line for a while finally concluding here at the end of this paragraph.
 *
 * The long description is ideal for more detailed explanations and
 * documentation. It can include example HTML, URLs, or any other information
 * that is deemed necessary or useful.
 *
 * @tag This is a tag named 'tag'
 *
 * TODO: This is a todo statement that describes an atomic task to be completed
 *   at a later date. It wraps after 80 characters and the following lines are
 *   indented by 2 spaces.
 */

/* Basic comment */

// Preprocessor style comments inside nested selectors & code explanations
```

Here's an example of the usage of our comment format in our codebase. You can find the [component file here](https://gitlab.com/SUSE-UIUX/eos/blob/master/assets/stylesheets/components/icons/installing.scss)

```scss
/* Installing icon
   ========================================================================== */
/**
*  Use it in HTML as
*  <div class='icon-installing md-18'></div>
*  add md-18, md-24, md-36 or md-48 class for sizes
*
*  the default icon size is 24px. Divided by 3 squares: 8px minus 2px padding between blocks = 6px
*/
// sass-lint:disable variable-for-property

/* Variables */
$icon-installing-bg: $sb-gray-800;
// 18px
$icon-size-18: md-18;
$icon-installing-block-18: 4px;
$icon-installing-margin-18: 7px;
$icon-installing-padding-18: 6px;
$icon-installing-padding-negative-18: -6px;

```

**Tools for your IDE**
These plugins add Idiomatic CSS comments to your code:
* Idiomatic CSS comments plugins:
* VS Code: https://bit.ly/2J0cTcJ
* Atom: https://bit.ly/2J1ikID
* Sublime Text: https://bit.ly/2su6RpH