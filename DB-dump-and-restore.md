### Backup your database
For our backup solutions, we're using MongoDB Nodejs Driver to dump the collections and Cloudinary as storage.  
To backup your database we're using the `api/mongodb` endpoint (see code in `routes/api/mongodb/index.js`).

You'll need to setup your Cloudinary API credentials env variables as follow: 
```js
// routes/api/mongodb/index.js, line 15
cloudinary.config({
  cloud_name: process.env.EOS_CLOUDINARY_NAME,
  api_key: process.env.EOS_CLOUDINARY_API_KEY,
  api_secret: process.env.EOS_CLOUDINARY_API_SEC
})
```
And also your database `EOS_DATABASE_URI_###`, `EOS_DATABASE_DB_###` and the enviroment variable you're runing EOS in `EOS_RUN_PROJECT_AS` (please refear to `env.template` for configuration.
```js
// routes/api/mongodb/index.js, line 22
const isDev = process.env.EOS_RUN_PROJECT_AS === 'dev'

  const uri = isDev
    ? process.env.EOS_DATABASE_URI_DEV
    : process.env.EOS_DATABASE_URI_PROD

  const databaseName = isDev
    ? process.env.EOS_DATABASE_DB_DEV
    : process.env.EOS_DATABASE_DB_PROD

 // ...
}
```


Once you define your variable, you can send a post request to http://localhost:3000/api/mongodb that will:
1.  Generate a dump folder inside the `./backup` folder in the main directory (you can change it by changing the variable `backupPath` in `/routes/api/mongodb/index.js`).
2.  It will compress the folder into a `.zip` file
3.  It will upload the compressed file into your Cloudinary space, inside `./DB` folder.
4.  It will remove the `./backup/` folder.


### Using the Migration Tool

####  IMPORTANT 1: We have a limiter to the endpoint to avoid spams to our backup endpoint (it's set to 1040 requests for development but just in case). You can skip it by commenting line `120 app.use('/api/mongodb/', limiter)` in our `app.js` file.

To get it running, we need several things:
1. Have MongoDB [utility tools ](https://docs.mongodb.com/manual/release-notes/4.4/#migration-to-mongodb-database-tools-project) install locally. For our Heroku instance we need to [add a plugin](https://elements.heroku.com/buildpacks/slategroup/heroku-buildpack-mongodump#buildpack-instructions)
2. Have the following env variables (the ones with the * are already part of our Heroku development instance and probably for your local dev env as well.)
```js
*process.env.EOS_RUN_PROJECT_AS 
*process.env.EOS_DATABASE_URI_DEV
*process.env.EOS_DATABASE_DB_DEV
process.env.EOS_DATABASE_URI_PROD
process.env.EOS_DATABASE_DB_PROD
```

With those things in place, run `npm start` and go to http://localhost:3000/internal/migration-tool
It will show you two sides panel with the development and production MongoDB instance (if any of the two are not showing, check your `env variables` that aim to the MongoDB URI and database name you want to read from`
1. Select the collections you want to merge into production
2. If you want a custom name, add it to the name field.
3. Run the application, there's gonna be some feedback related to the Work In Progress and completion if succeed.

If everything went right, check your MongoDB production instance for the new database as a result of the merge between both databases.

### Create a DB dump manually with mongodump

Sometimes you may need to connect to the Mongo DB when the application has crashed and there is no access to the DB from EOS. For these situations, use Mongo tools: https://docs.mongodb.com/manual/tutorial/backup-and-restore-tools/

To create a dump of all the DB in the cluster:

` mongodump  --uri <EOS_DATABASE_BACKUP_URI>`

This will download all the DB in a `dump/` folder locally where you run the command.

To restore a DB dump
` mongorestore --uri <EOS_DATABASE_BACKUP_URI> dump/<db-name> -d DB_NAME`

If you need to import data only, you can use [mongoimport](https://docs.mongodb.com/manual/reference/program/mongoimport/) or [mongoexport](https://docs.mongodb.com/manual/reference/program/mongoexport/) following the documentation from Mongo.