## What we do
We use Strapi as CMS where we define our pages title, descriptions and status (active/inactive).

## How we do
With every requests in our Express app, we make use of the middleware (`config-middleware.js`) that will  check if a route is defined in Strapi.
The three posible scenarios are the following:
- If the route is defined in Strapi, and the page enabled field it's set to true, the page will be rendered.
- If the route is defined in Strapi and the enabled field it's set to false, it will redirect your requests to `/dashboard`
- If the route is not defined in Strapi, it will set the files to default values, including setting enabled to true (see `config-middleware.js`)
 
To disallow a route, make sure the pages is defined (Strapi > Pages) and set the `enabled` field to false.

>  **NOTE**: If the env is development we ignore all the flags since we want to display all the pages, we achieve this by passing same object but with all the enabled values as true.

## Menu and submenu items.
To add new element to main menu and make use of the features flagging:
```
li(data-placement='right', title='PAGE_TITLE')
    a.js-select-current-parent.js-feature-flag(href='/PAGE_ROUTE', data-feature-flag= docEnabled['/PAGE_ROUTE'])
      i.eos-icons
        | miscellaneous
      span
        | PAGE_TITLE
```
For the submenu:
```
a.submenu-item.js-select-current.js-feature-flag(href='PAGE_ROUTE', data-feature-flag= docEnabled['PAGE_ROUTE'])
      | PAGE_TITLE
```


