---
Layout:
Title: " Back End Development and APIs"
Date: "2022 09 29"
---

# Introduction
Today I decided to go back to  Back End Development and APIs basic node and express.

# Body
Managing packages with npm-- npm (Node Package Manager), is a command line tool to install, create, and share packages of JavaScript code written for Node.js.One of the most common pieces of information in this file is the author field. It specifies who created the project, and can consist of a string or an object with contact or other details.An object is recommended for bigger projects.You can add the author like this :
"author": "Nosiphiwo Biyela",

Adding a Description to your package.json-- description is the string that should sell your idea to the user when they decide whether to install your package or not.This is how you add a description :
"description": "A project that does something awesome",

Adding keywords to your package.json -- The keywords field is where you can describe your project using related keywords.This is how you add keywords :
"keywords": [ "descriptive", "related", "words", "freecodecamp" ],

Adding a license to your package.json -- The license field is where you inform users of what they are allowed to do with your project.Some common licenses for open source projects include MIT and BSD. License information is not required, and copyright laws in most countries will give you ownership of what you create by default.This is how you add a license : 
"license":"MIT",

Adding a version to your package.json -- The version field describes the  current version of your project.This is how you add a version:
"version": "1.2.0",

Expanding your project with external packageds from npm -- Instead of manually having to make sure that you get all dependencies whenever you set up a project on a new computer, npm automatically installs everything for you.

We have a dependencies section on our package.json.In this section, packages your project requires are stored using the following format:

"dependencies": {
  "package-name": "version",
  "express": "4.14.0"
}

# Conclusion
I am still trying to understand how basic node and express works.I think everything will be clear once I start doing proects.