# EOS: Strapi integration

## Getting started
EOS depends on [Strapi](https://strapi.io/) for the configuration of the project and as a content management system. We use GraphQL with Strapi to query our data. You can find more at the [Strapi documentation](https://strapi.io/documentation/3.x.x/getting-started/quick-start.html#_5-consume-the-api) and [GraphQL Documentation](https://graphql.org/learn/)

After cloning EOS, make sure you set up and run a Strapi instance which will be used for content and storage of project data. 

We recommend using Heroku for the Strapi instance and MongoDB as database (you can get a free DB at [mlab](https://mlab.com/) by creating an account, or use the mlab plugin in Heroku).

⚠️ **Please note**: If you're using Heroku for you Strapi, the server is read-only (you cannot write any files) so generating models with Strapi is not possible. Make sure to do it locally then deploy back to Heroku.

## Configuring Strapi with Mongodb / Mlab
### Setting Strapi locally
