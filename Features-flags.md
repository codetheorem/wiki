## What we do
We use Gitlab [features flags](https://gitlab.com/SUSE-UIUX/eos/-/feature_flags) (they're using an Unleash server) to generate flags in order to control when we show/hide an element or route. 
When the new flags are created, make sure you set the flag name in the **EXACT** form as the route url.

**Example**: If we have the following route: `localhost:3000/buttons/buttons-icons` and we want to hide the subpage, we should create a new flag with the name of `buttons-icons`

## How we do
In order to avoid unnecessary network requests to Gitlab with each route requests to check for flags, when the servers lunch it'll generate a config file with flags status (`flags.config.js`. This will also help if for some reason Gitlab is not working, we still can use our application without interruptions) and this file it will be used with the middleware. If we want to update the config file without restarting the server (this is used to re-generate the file once a flag status is changed) we can do it at `http://localhost:3000/api/features` 
 
To allow/disallow a route, we make use of the features-toggle middleware (`modules/features-toggle.js`) that reads the `flags.config.js` and based on the feature status will allow or redirect the requests.  
>  If the env is development/staging we ignore all the flags since we want to display all the pages, we achieve this by passing an empty array.

## Menu and submenu items.
To show/hide an element from the menu:
```
 a(href='/buttons', class= path.match(/\/buttons.*?/) ? 'active' : '', class= flags.buttons.enabled ? '' : 'hidden')
```

A second `class` is needed since we can't nest more statements where we add a class of `hidden` if the flag is set to disable.

IMPORTANT: If the route is single word (`buttons`) we can use dot notation (`flags.buttons.enabled`) to check for the status. If we have multiple words separated by `-` make sure you use bracket notation (`flags['when-to-use-them'].enabled`)

