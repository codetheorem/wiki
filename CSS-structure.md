[◀️ Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#writing-code)


Structuring our Sass files is important since it will help us to keep a cleaner, more consistent and reusable code. Keeping a structured mindset when defining our CSS will help us avoid technical debt in the near future.

We structure our CSS files is inspired by the [SMACSS](https://smacss.com) convention but also other patterns, such as the [7-1 pattern](https://sass-guidelin.es/#the-7-1-pattern).

Currently, we're compiling all files into a single one. Such structure allows us to use a web components-inspired approach, in which we can use and compile only the CSS that is relevant to a specific component.

## Our current Sass structure explained
We have the following folders:
* eos-base
* eos-custom-base
* eos-components
* eos-custom-components
* eos-elements
* eos-layout
* eos-pages

### Base
This is where we define all those essential bits of our page, such as variables & typography. They style Bootstrap's base styles. [Link](https://gitlab.com/SUSE-UIUX/eos/tree/master/assets/stylesheets/eos-base)

### Custom base
In here we define our own base styles. [Link](https://gitlab.com/SUSE-UIUX/eos/tree/master/assets/stylesheets/eos-custom-base)

### Components
This is where we include Bootstrap components that use EOS styles. [Link](https://gitlab.com/SUSE-UIUX/eos/tree/master/assets/stylesheets/eos-components)

### Custom components
Here we include the styles for the components defined by us. [Link](https://gitlab.com/SUSE-UIUX/eos/tree/master/assets/stylesheets/eos-custom-components)

### Elements
In this folder, we include basic elements such as buttons or icons. [Link](https://gitlab.com/SUSE-UIUX/eos/tree/master/assets/stylesheets/eos-elements)

### Layout
Here we include all the styles that are used to define the look & feel of the layout we use. [Link](https://gitlab.com/SUSE-UIUX/eos/tree/master/assets/stylesheets/eos-layout)

### Pages
In this folder, we include the styles that are specific to custom features in pages. [Link](https://gitlab.com/SUSE-UIUX/eos/tree/master/assets/stylesheets/eos-pages)