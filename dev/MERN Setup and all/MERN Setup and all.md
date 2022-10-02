**Backend Quick Start**

1. Express – make an instance of express by const **app = express()**

1. For middlewares use() is used. They get included throughout the app.

eg **app.use(cors());**

1. Router instance = 

const **router = express.Router()** ---- Used to split the routes, making easier to debugg and code 

**then use it as router.get()/post()/all() like app**

export router and include it in index.js using middleware .

1. Form data types:
- application/x-www-form-urlencoded: This value represents a URL (Uniform Resource Locator) encoded form. By default, it is assigned to the *enctype* attribute.
- multipart/form-data: This value represents a m*ultipart* form. It is used to upload files by the user.
- text/plain: This value represents a form that is newly introduced in the latest HTML5 which is used to send the data without any encoding.

When post request is made by HTML form, it is sent as body of request. To extract this we need to use express.urlencoded() middleware:

const express = require('express')

const app = express()

app.use(express.urlencoded({

`  `extended: true

}))



