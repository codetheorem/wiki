Currently we are manually copy-pasting data in our PUG file to shows the different example snippet of SCSS and HTML code and this can bring human error, it isn't scalable because we will always have to go back to the files to find and copy-paste the code, and it isn't maintainable as when something changes in the code it isn't automatically reflected in the UI in the code snippets. 

### SCSS files

Currently, we have only one SCSS file for one component. **For Example**, buttons.component.scss has CSS classes for all the buttons types, like default button class and primary button class. We can split this single file into multiple files and create one file for each button type. 

**gulp-split-files** URL: https://www.npmjs.com/package/gulp-split-files 

**Problem:**

It will create duplication of code. ( but we can delete these files once we retrieve data from it)

** Good:**

 It will create separate files for each class which will be easy to use.

**Or**

Create a separate single file for each class or button type. 
For example button.scss, default-button.scss etc.

### Autofill data

Once separate files for each class or element types are ready you can use a service to pull these files and then use a controller to display code from SCSS file to the HTML page.