---
Layout:
Title: " Back End Development and APIs"
Date: "2022 09 26"
---


# Introduction
Today I was busy with Back End Development and APIs.

# Body
Serve JSON on a Specific Route -- A REST (REpresentational State Transfer) API allows data exchange in a simple way, without the need for clients to know any detail about the server. The client only needs to know where the resource is (the URL), and the action it wants to perform on it (the verb).The GET verb is used when you are fetching some information, without modifying anything. 

e.g Let's create a simple API by creating a route that responds with JSON at the path /json. You can do it as usual, with the app.get() method. Inside the route handler, use the method res.json(), passing in an object as an argument. This method closes the request-response loop, returning the data. Behind the scenes, it converts a valid JavaScript object into a string, then sets the appropriate headers to tell your browser that you are serving JSON, and sends the data back. A valid object has the usual structure {key: data}. data can be a number, a string, a nested object or an array. data can also be a variable or the result of a function call, in which case it will be evaluated before being converted into a string :

app.get("/json", function(req, res) {

  res.json({"message": "Hello json"});

});


Use the .env File -- The .env file is a hidden that is used to pass environment variables to your application.This file is secret,you can only access it and it can be used to store data that you want to keep private or hidden.The environment variables are accessible from the app as process.env.VAR_NAME .The process.env object is a global Node object, and variables are passed as strings. By convention, the variable names are all uppercase, with words separated by an underscore. There cannot be space around the equals sign when you are assigning values to your variables, e.g. VAR_NAME=value

e.g Let's add an environment variable as a configuration option.Create a .env file in the root of your project directory, and store the variable MESSAGE_STYLE=uppercase in it.In the /json GET route handler you created in the last challenge access process.env.MESSAGE_STYLE and transform the response object's message to uppercase if the variable equals uppercase.The response object should either be {"message": "Hello json"} or {"message": "HELLO JSON"}, depending on the MESSAGE_STYLE value:

app.get("/json", function(req, res) {

if(process.env.MESSAGE_STYLE === 'uppercase') {

  res.json({"message": "Hello json".toUpperCase()})

}else{

  res.json({"message": "Hello json"})

}

});

# Conclusion
For now I don't understand what back end is about but I am going to continue practicing. 