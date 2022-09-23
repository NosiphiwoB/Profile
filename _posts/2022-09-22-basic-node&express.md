---
Layout:
Title: " Back End Development and APIs"
Date: "2022 09 22"
---

# Introduction
Today I was busy with Basic Node and Express.

# Body
Managing npm Depencies by understanding semantic versioning -- Versions of the npm packages in the dependencies section of your package.json file follow what’s called Semantic Versioning (SemVer), an industry standard for software versioning aiming to make it easier to manage dependencies.SemVer can be useful when you develop software that uses external dependencies.This is how Semantic Versioning  works : 

"package": "MAJOR.MINOR.PATCH" 

The MAJOR version should increment when you make incompatible API changes. The MINOR version should increment when you add functionality in a backwards-compatible manner. The PATCH version should increment when you make backwards-compatible bug fixes. This means that PATCHes are bug fixes and MINORs add new features but neither of them break what worked before. Finally, MAJORs add changes that won’t work with earlier versions.

e.g "dependencies": {

    "@freecodecamp/example": "1.2.13",
    
    }
    
Using the Tilde-Character to always use the latest patch version of a  dependency -- To allow an npm dependency to update to the latest PATCH version, you can prefix the dependency’s version with the tilde (~) character. Here's an example of how to allow updates to any 1.3.x version: "package": "~1.3.8" .

To use the latest minor version of a dependency we use the Caret-Character -- The caret (^) allows npm to install future updates,the differnce is that the caret will allow both Minor updates and patches.

e.g "dependencies": {

    "@freecodecamp/example": "^1.2.13",

	},


Removing a package from our dependencies -- You just remove the corresponding key-value pair for that package from your dependencies.

Basic node and express

We have a fundamental method called  app.listen(port),it tells your server to listen on a given port putting it in running state.We need the app to be running in te background for testing purpose

In Express ,routes takes the following structure: app.METHOD(PATH,HANDLER).METHOD is an http method in lowercase. PATH is a relative path on the server (it can be a string, or even a regular expression). HANDLER is a function that Express calls when the route is matched. Handlers take the form function(req, res) {...}, where req is the request object, and res is the response object.This is how you write a handler:

app.get("/", (req, res) => {

   res.send("Hello Express");

}) --> this will serve the string "Hello Express".

Serving an HTML File -- you can respond to requests with a file using the res.sendFile(path) method. You can put it inside the app.get('/', ...) route handler.This file needs an absolute file path,Node global variable __dirname is recommended to use to calculate the path like this :

absolutePath = __dirname + relativePath/file.ext

# Conclusion
At the moment I'm having issues understanding back end development but I will watch some youtube tutorials.