We use [Prism.js](https://prismjs.com/) to display code snippets. Creating a code snippet is very simple:

```

pre.js-snippet-code
 template.js-code-template
   | transition: all 0.5s ease-out
 code.js-code-render.language-css

```

```
pre.js-snippet-code
  template.js-code-template
    | <div class='alert alert-global alert-success'>
    |   <i class='eos-icons eos-18'>check_circle</i>
    |   <div class='alert-body'>
    |     <div class='alert-global-desktop'>Your account has been successfully migrated to the new user interface.</div>
    |     <div class='alert-global-mobile'>Your account has been migrated.</div>
    |   </div>
    |   <a class='close' data-dismiss='alert'><i class='eos-icons eos-18'>close</i></a>
    | </div>
  code.js-code-render.language-html
```

- `template.js-code-template` is where we add our code example, in plain HTML, SCSS, JS, CSS.
- `code.js-code-render.language-html` here the code will render. We need to specify what language it is with `language-`. [List of supported languages](https://lucidar.me/en/web-dev/list-of-supported-languages-by-prism/) (some don't come by default, they need to be set up).
