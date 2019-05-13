Currently we are manually copy-pasting data in our PUG file to shows the different example snippet of SCSS and HTML code and this can bring human error, it isn't scalable because we will always have to go back to the files to find and copy-paste the code, and it isn't maintainable as when something changes in the code it isn't automatically reflected in the UI in the code snippets. 

## SCSS code
**gulp-split-files** URL: https://www.npmjs.com/package/gulp-split-files 

 Currently, we have only one SCSS file for one component. For Example, buttons.component.scss has CSS classes for all the buttons type, like default button class and Primary button class. We can split this single file into multiple files and create one file for each button types.    

**Problem:**

It will create duplication of code.( but we can delete these files once we retire data from it)

** Good:**

 It will create separate files for each classes which will be easy to use.