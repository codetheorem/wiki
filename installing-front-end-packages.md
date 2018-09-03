### How to install a new FE package

You will notice that we have a `node_modules` folder in the root that is managed by our main `package.json` in the root. This is where we save all packages we use for operations (building, testing, etc) and backend (node + express).

But, when you run `npm install` you will see that a new `node_modules` folder is created under the `vendors` folder. This `vendors/node_modules` folder is managed by the `vendors/package.json` file.
In order to install a new front-end package you need to run the normal `npm i ...` but being under the right path in your terminal, meaning `vendors`, so the first step when installing a FE package is that you do

`cd vendors`

and then

`npm i --save PACKAGE_NAME` (always use --save, otherwise it wont work, since --save-dev is skipped in Heroku)

### How to add the package to be compiled

Once you had saved it into `vendors/package.json`, then in the same file you will find the object `mainfiles`. Here you have to create a new object following the format it has currently, where the property is the exact name of the package's folder (normally the same name as the package itself), and the value of this property should be an array of strings, where the name of the file/folder should always begin with a `/`


example:

```
"mainfiles": {
    "jquery": [
      "/dist/jquery.min.js"
    ]
}
```

Once you have included there the name of the file/s you need, you only need to run `gulp` and it will take care of compiling the new vendor files.

NOTE: if you never install a new package, you dont need to run `gulp` at all, since it is triggered once when you run `npm install` in the root of the repository. `gulp` is only useful if you already installed all packages for EOS and added/changed a FE package (development reasons)