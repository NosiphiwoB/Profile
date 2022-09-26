---
Layout:
Title: " Back End Development and APIs"
Date: "2022 09 23"
---

# Introduction
Today I was busy with back end development and apis,I also did a revision on react.

# Body
Serve Static Assets-- An HTML server usually has one or more directories that are accessible by the user. You can place there the static assets needed by your application (stylesheets, scripts, images).In Express, you can put in place this functionality using the middleware express.static(path), where the path parameter is the absolute path of the folder containing the assets.

A middleware needs to be mounted using the method app.use(path, middlerwareFunction).The first path argument is optional,if you don't pass it the middleware will be exexuted for all requests.

e.g Mount the express.static() middleware to the path /public with app.use(). The absolute path to the assets folder is __dirname + /public:

app.use("/public", express.static(__dirname + "/public")); 

I didn't do much on back end development and apis as I had to make time and prepare for the react that we are goig to have soon.

# Conclusion
I am going to continue with back end development and I will also revision on react.
