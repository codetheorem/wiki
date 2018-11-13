For some situations in order to test something locally we need to make use for some `env variables`.
Right now we're not using any library for it (in the future we'll implement dotenv or similar).

Setup instructions 
----
[Setup env variables in MacOS: Bash](https://medium.com/@himanshuagarwal1395/setting-up-environment-variables-in-macos-sierra-f5978369b255)  
[Setup env variables in MacOS: Fish](https://stackoverflow.com/questions/25632846/how-to-set-environment-variables-in-fish-shell)  

Example of use
----
```js
var transporter = nodemailer.createTransport({
    service: 'gmail',
    auth: {
      user: 'email@adress.com',
      pass: process.env.SMTP_TOKEN
    }
  })
```

Important
----
We only share the values via PM, so make sure you ask the team for them