---
Layout:
Title: " Back End Development and APIs"
Date: "2022 09 28"
---

# Introduction
Today I was busy with back end development and apis.

# Body
Chain middleware to create a time server -- Middleware can be mounted at a specific route using app.METHOD(path, middlewareFunction).Middleware can also be chained within a route definitaion.

e.g app.get("/user", function(req, res, next) {

    req.user = getTheUserSync(); //Hypothetical synchronous operation

    next();

    }, function(req, res) {

    res.send(req.user);

    });
    
This is useful to split the server operations into smaller units, which to better app structure and the possibility to reuse the code in different places.This approach can also be used to perform some validation on the data.At each point of the middleware stack you can block the execution of the current chain and pass control to functions specifically designed to handle errors. You can pass control to the next matching route to handle special cases.

Here is another example :
In the route app.get('/now', ...) chain a middleware function and the final handler. In the middleware function you should add the current time to the request object in the req.time key. You can use new Date().toString(). In the handler, respond with a JSON object, taking the structure {time: req.time}:

app.get("/now", function(req, res, next) {

  req.time = new Date().toString();

  next();

}, function(req, res) {

  res.send({time: req.time});

});
    
Get Route Parameter Input from the Client -- When building an API, we have to allow users to communicate to us what they want to get from our service. We can achieve this result by using route parameters.Route parameters are named segmments of the URL, delimited by slashes (/).Each segment captures the value of the part of the URL which matches its position.The captured values can be found in the req.params object.

e.g Build an echo server, mounted at the route GET /:word/echo. Respond with a JSON object, taking the structure {echo: word}. You can find the word to be repeated at req.params.word. You can test your route from your browser's address bar, visiting some matching routes, e.g. your-app-rootpath/freecodecamp/echo:

app.get("/:word/echo", function(req, res) {

  const {word} = req.params;

  res.json({

    echo: word

  });

})


Get Query Parameter Input from the Client -- Another common way to get input from the client is by encoding the data after the route path, using a query string.The query string is delimited by a question mark (?), and includes field=value couples. Each couple is separated by an ampersand (&). Express can parse the data from the query string, and populate the object req.query.Some characters, like the percent (%), cannot be in URLs and have to be encoded in a different format before you can send them. 

e.g app.get("/name", function(req, res) {

  const { first: firstName, last: lastName} = req.query;

 res.json({
    
   name:` `${firstName} ${lastName}` `

 });

});


Use body-parser to Parse POST Requests -- POST is the default method used to send client data with HTML forms.In REST convention, POST is used to send data to create new items in the database (a new user, or a new blog post). 

e.g 
let bodyParser = require("body-parser"); 

app.use(bodyParser.urlencoded({extended:false})) 

app.use(bodyParser.json())

app.get("/body-parsed-info", function(req, res) {

  res.json({ parsed: bodyParser.json() });

});

# Conclusion
I am going to move on to MongoDB and Mangoose.