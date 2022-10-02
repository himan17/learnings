**Backend:**

Heroku:

1) Heroku procfile:

web:node index.js
- ![](Aspose.Words.2bbab34b-ce89-4dad-9b5e-c134f99a3331.001.png)Create Procfile in server folder. It has no extension. Paste this to the file:

- Add this to start scripts in the package.json

"engines": {

`    `"node": "16.15.0"

`  `},

`  `"description": "",

`  `"main": "index.js",

`  `"scripts": {

`    `"start": "node index.js"

`  `},


![](Aspose.Words.2bbab34b-ce89-4dad-9b5e-c134f99a3331.002.png)

- Make sure your port in index.js is set to process.env.PORT || 8000

- If you have dotenv file make sure to set config var in heroku. This can be done :

Heroku > login > app > settings > reveal config vars > add key: value from .env file to their boxes.

- If you are using API for frontend calls then you must add cors in index.js : which allows to make cross domain calls. 
1) **Errors**: Do not upload node modules in git. Else there might be some error on heroku. If you upload accidently then you need to delete those files from git and then push to heroku again:

git rm -rf node\_modules

**Frontend:**

Netlify:

1) For netlify we just need build file to be uploaded. Run this to create build file

npm run build

1) Handling Redirects: Netlify will throw errors when a page is reloaded. To fix this we need to create a file in build folder:

Client > build > \_redirects

In the redirects, we need to paste this:

/\*  /index.html  200
