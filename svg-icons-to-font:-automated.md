### Investigations:

**1)** gulp-iconfont 
URL: https://www.npmjs.com/package/gulp-iconfont

**Problems:** 
- It requires Gulp, which we dont use. To use it we would have to invest extra time configuring and maintaining a gulp builder. 
- Requires svg in 500min height, contrary to our icon design guidelines, which would mean extra work exporting designing in 24px but exporting to 500px.
- No option for ligature

**Good:** 
- Has plenty of daily downloads which means: more chances it is well maintained.

**Evaluation:** 2/5


**2)** iconfont-maker
URL: https://www.npmjs.com/package/iconfont-maker

**Problems:** 

- Doesn export less
- Doesnt accept ligatures
- Only a few downloads a week. Doesnt seem to be a popular module.

**Good:** 

- Npm package we can manipulate in nodejs or perhaps simply as a script in package.json
- Exports scss

**Evaluation:** 1/5

**3)** svg-font-create
URL: https://www.npmjs.com/package/svg-font-create

**Problems:**

- The library is old and it was last updated 4 years ago. 
- Outdated dependencies.

**Evaluation:** 1/5

**4)** icon-font-generator
URL: https://www.npmjs.com/package/icon-font-generator

**Problems:**

- Cant process LESS/SCSS
- Cant create ligatures

**Good:**

- Accepts multiple (single icon) svg files
- Npm package we can manipulate in nodejs or perhaps simply as a script in package.json.
- Popular and has many downloads. Last updated 5 months ago.

**Evaluation:** 2/5

**5)** svgicons2svgfont
URL: https://www.npmjs.com/package/svgicons2svgfont

**Problems:**

- Doesnt take care of CSS, at all

**Good:**

- It seems to be the original module all others are integrating inside.
- The most popular module seen.
- Last updated 1 month ago.
- Handles multiple svg files.
- Extracts ligatures from the file name.
- If an icon has shapes not merged into 1 path, it will take care of merging them.
- From this project come the following options:

a) https://www.npmjs.com/package/grunt-webfont
b) https://github.com/nfroidure/gulp-iconfont
c) https://github.com/nfroidure/gulp-svgicons2svgfont
d) https://www.npmjs.com/package/webfonts-generator





**Problems:**

-

**Good:**

-