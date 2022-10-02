const multer = require('multer');

const fileStorageEngine = multer.diskStorage({

`    `destination: (req, file, cb)=>{

`        `cb(null, './uploads')

`    `},

`    `filename: (req, file, cb)=>{

`        `cb(null, Date.now()+'-'+file.originalname);

`    `}

});

const upload = multer({

`    `storage: fileStorageEngine, 

`    `limits: {fileSize: 20000000}

});

const postUpload = upload.fields({name: "post\_media", maxCount: 10});

router.post('/create-post',checkAuth, function (req, res) {

`        `postUpload(req, res, function (err) {

`            `if (err) {

`                `return res.status(400).send({ message: err.message, Desired\_format: "multipart form with 'post\_text' for text content and 'post\_media' for all post files"})

`            `}

`            `if(!req.body.post\_text){

`                `res.status(400).send({ message: err.message, Desired\_format: "multipart form with 'post\_text' for text content and 'post\_media' for all post files"})

`            `}

`            `// Everything went fine.



`            `console.log("body", req.body, req.file);

`            `res.json({success:true});

`        `});

`    `}

)

**What Is a Data URI?**

*A data URI is a base64 encoded string that represents a file. Getting the contents of a file as a string means that you can directly embed the data within your HTML or CSS code. When the browser encounters a data URI in your code, it’s able to decode the data and construct the original file.* 


Error [ERR\_HTTP\_HEADERS\_SENT] is an interesting error that is fired up when a server tries to send more than one response to a client. What this means is that for a given client request the server previously sent a response (either a success responsei with the resource requested or error response for a bad request) back to the client and now is **unexpectedly** trying to send another response
