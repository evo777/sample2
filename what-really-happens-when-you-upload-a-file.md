##Order of events

1. A form element encoded as "multipart/form-data" is required to take file' inputs
  * multipart/form-data enables entire files to be included in data.
  * Setting an input to 'file' enables the user to select a file
2. Submitting the form sends a post request to the server
3. Using node / express, the file info can be accessed in the req.files object
4. The server reads the data of the uploaded file (fs.readfile)
5. The server writes the file to a directory path (fs.writefile)

##Helpful tools
* [multer](https://github.com/expressjs/multer) - Node/Express middleware for handling file uploads
* [sharp](https://github.com/lovell/sharp) - Node module that resizes, compresses, and converts images
* [new FormData()](https://developer.mozilla.org/en-US/docs/Web/API/FormData/Using_FormData_Objects) - Instead of an HTML form, create a form data object in javascript to send as a post request.