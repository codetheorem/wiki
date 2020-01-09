# EOS: Strapi integration

## Getting started
EOS depends on [Strapi](https://strapi.io/) for the configuration of the project and as a content management system. We use GraphQL with Strapi to query our data. You can find more at the [Strapi documentation](https://strapi.io/documentation/3.x.x/getting-started/quick-start.html#_5-consume-the-api) and [GraphQL Documentation](https://graphql.org/learn/)

After cloning EOS, make sure you set up and run a Strapi instance which will be used for content and storage of project data. 

We recommend using Heroku for the Strapi instance and MongoDB as database (you can get a free DB at [mlab](https://mlab.com/) by creating an account, or use the mlab plugin in Heroku).

⚠️ **Please note**: If you're using Heroku for you Strapi, the server is read-only (you cannot write any files) so generating models with Strapi is not possible. Make sure to do it locally then deploy back to Heroku.

## Configuring Strapi with Mongodb / Mlab
### Setting Strapi locally

1. Clone our Strapi repository https://gitlab.com/SUSE-UIUX/eos-strapi 
2. Create a local mongodb database: https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/
   * Or create it in the cloud with https://cloud.mongodb.com or https://mlab.com/. You’ll require a connection URI and the name of the DB to setup the connection with Strapi.
   * More info about mongoDB URI format https://docs.mongodb.com/manual/reference/connection-string/
3. You'll need to set up two local variables in order for Strapi to connect to your database. (see Development and Production variables names below)
4. You can start Strapi by running npm start.

💡 **NOTE**: you can run Strapi in development or production by changing `NODE_ENV`.
eg: `env NODE_ENV= production npm start`
