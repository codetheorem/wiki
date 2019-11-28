◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#writing-code)


Structuring our Sass files is important, since it will help us to keep a cleaner, more consistent and reusable code. Keeping a structured mindset when defining our CSS will help us avoid technical debt in the near future.

We structure our CSS files is inspired by the [SMACSS](https://smacss.com) convention but also other patterns, such as the [7-1 pattern](https://sass-guidelin.es/#the-7-1-pattern).

Currently, we're compiling all files into a single one (except for landing pages) but using a structure such as ours allows us to use a web components-inspired approach, in which we can use and compile only the CSS that is relevant to a specific component.

## Our current Sass structure explained
We have the following folders:
* base
* components
* helpers
* landing-page
* layout
* vendor

### Base
This is where we define all those essential bits of our page, such as variables & typography. Within this folder, variables have also been structured into subfolders. 

### Layout
Here we add all the layout definitions such as the main structure of our document, header, footer, etc.

### Components
This is where all the micro layout items are included. Examples are: badges, icons, labels, loaders, etc.

### Helpers
Helpers are files that manage animations, mixins functions. Usually files that won't compile (except with animations)

### Landing page
This folder includes all the styles relevant to this Design System's homepage. Due to the nature of the project, we won't have many landing pages. If this is the case in the future, we could include a `pages` folder in our main structure.

### Vendor
Here we add all vendor overrides. We currently have Twitter Bootstrap