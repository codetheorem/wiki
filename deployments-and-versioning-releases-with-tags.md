[Back](https://gitlab.com/SUSE-UIUX/eos/wikis/home#developing-the-eos-project)

# Continuous integration with Gitlab CI

Our CI is configured to continuously deploy to our staging server (with URL: http://eos-test.herokuapp.com) every time a PR is merged into the Master branch.

All PR's should be opened to merge against Master and not any other branch unless specifically required to do so.

# Tags and versions

Master will always hold the latest and most updated version of our application, although unstable and not ready to be published internally, while stable releases will be tagged and published by our PO (Cynthia Sanchez) when all cards in the **Current (now)** column in the EOS project roadmap are marked as done.

A tag can be created before all items in the roadmap are done if the PO suggests there is an important patch or feature our consumers would benefit from having.

We will follow the Semantic Versioning (http://semver.org/) as follows below:

### Given a version number MAJOR.MINOR.PATCH, increment the:

MAJOR version when you make incompatible API changes, changes in 
MINOR version when you add functionality in a backwards-compatible manner, and
PATCH version when you make backwards-compatible bug fixes.
Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

Once a versioned package has been released, the contents of that version MUST NOT be modified. Any modifications MUST be released as a new version.

# Deploying to production

Deployment to production is manual and it is available in gitlab for the PO or deputy PO to deploy once the work is ready to be published.
WARNING: the pipeline might let other members of the team deploy to production, please avoid this action and only let PO decide when it is ready to be deployed.

# Test production in local environment

**How it works:**  
We use the build-in env variables created by node. The default value is `development` and in heroku it's set to `production`.

----
**Hide content from production:**  
To hide the content, we do  
```
- if (process.env.NODE_ENV != 'production') { 
  Code that would be hide from production
- }
```

This part would show the content in our `localhost`or `eos-test` website but not our `production` site without any extra changes in our  `npm scripts` 

----
**Test production locally:**  
To test production locally run `npm run env:prod`.