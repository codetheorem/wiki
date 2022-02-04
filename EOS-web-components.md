[◀️ Back](https://gitlab.com/SUSE-UIUX/eos/-/wikis/home#eos-web-components)

## Development
We use Polymer CLI for serving/building, please follow [Getting Started](https://lit-element.polymer-project.org/guide/start). 

Once you get Polymer, clone the repository: [EOS / EOS-webcomponents](https://gitlab.com/SUSE-UIUX/EOS-webcomponents) and run `npm install` followed by `polymer serve` to start a development env.

### Create web components
**Get started:** [Templates](https://lit-element.polymer-project.org/guide/templates), [Styles](https://lit-element.polymer-project.org/guide/styles), [Properties](https://lit-element.polymer-project.org/guide/properties)

When writing new components to display it, it's done with the return HTML `templateString`.

**Example:**
```
lass EosAlert extends LitElement {
  MORE CODE GOES HERE…
render () {
   return html`
     <div class='alert ${this.type} ${this.scope}'>
       <i class="alert-icon eos-icons md-18">${this.icon[this.type]}</i>
       <div class='alert-body'>
       <div class='alert-title ${(this.title || 'hide')}'> ${this.title} </div>
       <p> <slot/> </p>
     </div> 
...

```

### Styling a component
**Get started**: [Styles](https://lit-element.polymer-project.org/guide/styles)

Creating the component I thought it would be a good idea to use HTML variables for colors, we can provide an eos-variables.css with them and it only has to be loaded once. Every component can access them once we assign the variables to the :root {}

Check variables names under `assets/eos-variables.css`

You can access variables as shown here:
```css
.section.success,
   .inline.success {
     background-color: var(--eos-bc-green-100);
     border-color: var(--eos-bc-green-500);
   }
...

```
Each component has his own isolated style, check the Style getting started to learn more. 

**Example:**
```
static get styles () {
   return css`
   /* ==== General==== */
   .alert {
     border-left: 5px solid var(--eos-bc-green-500);
     display: flex;
     margin-bottom: 20px;
     margin: 16px;
...

```


## Publishing
### Implementation without Node.js

First, we need to bundle all our code and dependencies, the project has already a command for that called `npm run bundle` that will bundle everything with bable and rollup.
Once you run the command, a folder build will be generated with `eos-components.bundle.js` inside. This is the file that will include all our components (alerts, buttons…) and you have to import it in your project.

Necessary files for the components are: 
- eos-variables.css 
- eos-components.bundle

Then in your project, including the files in the project header with eos-icons CDN for the icons.

```html
<link rel="stylesheet" href="eos-variables.css">
<script src="eos-components.bundle.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/eos-icons/dist/extended/css/eos-icons-extended.css" />

```

And to use the component:
```html
<eos-alert type='info' scope='section' title="Success alert!">
  Lorem ipsum dolor sit amet consectetur.
</eos-alert>
```

**DEMO**: [https://codepen.io/en3sis/pen/abzqKPW](https://codepen.io/en3sis/pen/abzqKPW)


## Implementation in React (or Angular)
For frameworks, we can deliver npm packages with the components without the bundle.

We just need to add the lit-element package to our project `npm install lit-element`
- Then copy the `components` and `assets` folders.
- In your index.html file, import [eos-icons CDN link ](https://cdn.jsdelivr.net/npm/eos-icons/dist/extended/css/eos-icons-extended.css)
- Import both files and we can mount the component as the example below
```
import React from "react";
import ReactDOM from "react-dom";
/* EOS WEB COMPONENTS */
Import "./eos-variables.css";
import "../components/alerts/index";
 
function App() {
 return (
   <div className="App">
     <h1>React APP</h1>
     <h2>Testing custom element</h2>
 
     <eos-alert type="warning" scope="global">
         Lorem ipsum dolor sit amet consectetur elit. 
     </eos-alert>
...

```

DEMO:  [https://codesandbox.io/s/custom-component-react-pmfor](https://codesandbox.io/s/custom-component-react-pmfor)
