### Investigations:

**1)** gulp-iconfont 
URL: https://www.npmjs.com/package/gulp-iconfont

**Problems:** 
- It requires Gulp, which we dont use. To use it we would have to invest extra time configuring and maintaining a gulp builder. 
- No option for ligature

**Good:** 
- Has plenty of daily downloads which means: more chances it is well maintained.

**Evaluation:** 2/5


**2)** iconfont-maker
URL: https://www.npmjs.com/package/iconfont-maker

**Problems:** 

- Doesn export less
- Doesnt accept ligatures
- Only a few downloads a week. Doesnt seem to be a popular library.

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
- Popular library.
- Last updated 1 month ago.
- Handles multiple svg files.
- Extracts ligatures from the file name.
- If an icon has shapes not merged into 1 path, it will take care of merging them.
- From this project come the following options:

a) https://www.npmjs.com/package/grunt-webfont

**Problems:**

- We dont use Grunt in any project (no actual experience within the team) and it seems a bit pointless to have it only for 1 task.

**Good:**

- Can export css, sass, scss or less.
- Popular enough and well maintained.
- Exports HTML demo page.
- Supports ligatures with fontforge (default engine).


b) https://github.com/nfroidure/gulp-iconfont

**Problems:**

- It requires Gulp, which we dont use. To use it we would have to invest extra time configuring and maintaining a gulp builder. 

--- It is generally the same as the one below

c) https://github.com/nfroidure/gulp-svgicons2svgfont

**Problems:**

- It requires Gulp, which we dont use. To use it we would have to invest extra time configuring and maintaining a gulp builder. 

**Good:**

- Exports css/scss
- CLI usage.
- Generates CSS files and HTML preview, allows using custom templates.
- Very popular library.
- Last updated 1 month ago.

d) https://www.npmjs.com/package/webfonts-generator


**Problems:**

- Only exports css.
- Last updated 9 months ago.

**Good:**

- CLI usage.
- Generates CSS files and HTML preview, allows to use custom templates.
- Good popularity.




ALL: All libraries require a minimum height of 500px in the SVGs.

