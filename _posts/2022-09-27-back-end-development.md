---
Layout:
Title: " Back End Development and APIs"
Date: "2022 09 27"
---

# Introduction
Today I was busy with back end development and apis .

# Body
Today I had so much issues, I did everything that was required but the test was not passing.I was only able to do one challenge.

Implement a Root-Level Request Logger Middleware -- Middleware functions take 3 arguments: the object,the response object, and the next function in the application's request-response cycle.These functions execute some code that can have side effects on the app, and usually add information to the request or response objects. They can also end the cycle by sending a response when some condition is met.If they don’t send the response when they are done, they start the execution of the next function in the stack. This triggers calling the 3rd argument, next().

eg If you want to build a simple logger:

app.use("/", function(req, res, next) {

 console.log(req.method + " " + req.path + " - " + req.ip);

  next();

});


# Conclusion
I am goinh to continue with  bac end development.