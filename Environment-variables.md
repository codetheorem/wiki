◀️ [Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#project-setup)


For some situations, in order to test something locally, we need to make use of some `env variables`. All environment variables in EOS are set up in an `.env` file found in the root of the project. 


Setup instructions 
----

Since the file includes sensitive data, we have included a template file (`.env.template`). You'll need to rename this file to "`.env`" and add the passwords there. All new environment variables should be added to this file. The file is included in the project's `.gitignore`. It should **always** stay ignored and never pushed into the repository.


```
Current variables
----
```js
/* SMTP */
process.env.SMTP_EMAIL
process.env.SMTP_TOKEN
/* Google Tag Manager (production only) */
EOS_GTM_ID
/* Cloudinary */
EOS_CDN_API_KEY
EOS_CDN_API_SEC
EOS_CDN_NAME
/* Strapi CMS */
EOS_STRAPI_PASSWORD_DEV
EOS_STRAPI_SERVER_DEV
EOS_STRAPI_USERNAME_DEV
```

**Important notes for maintainers only**
----
We only share the values via PM, so make sure you ask the team for them. The keys for the different environment variables are found in our hosting provider's settings.

## Using local variables

### Using bash

[Setup env variables in MacOS: Bash](https://medium.com/@himanshuagarwal1395/setting-up-environment-variables-in-macos-sierra-f5978369b255)

example:

```
export DB_CONNECTION=STRING_HERE
```


### Using fish  
[Setup env variables in MacOS: Fish](https://stackoverflow.com/questions/25632846/how-to-set-environment-variables-in-fish-shell)  


example:

**Set a new var**
```
set -Ux EOS_VAR_NAME STRING_HERE
```

**Unset (delete) var**
```
set -e EOS_VAR_NAME
```

**Print all vars**
```
printenv
```

