---
Layout:
Title: "Javascript tutorials"
Date: "2022 05 18"
---


# Introduction
Today I was busy with javascript revision.I have decided that I going to go back and do javascript again on freecode camp.

# Body 
In JavaScript all variables and function names are case sensitive. This means that capitalization matters.

MYVAR is not the same as MyVar nor myvar. It is possible to have multiple distinct variables with the same name but different casing. It is strongly recommended that for the sake of clarity, you do not use this language feature.

e.g
var studlyCapVar;

var properCamelCase;

var titleCaseOver;

studlyCapVar = 10;

properCamelCase = "A String";

titleCaseOver = 9000;

One of the biggest problems with declaring variables with the var keyword is that you can easily overwrite variable declarations
e.g 
var camper = "James";

var camper = "David";

console.log(camper);

The camper variable is originally declared as James, and is then overridden to be David. The console then displays the string David

A keyword called let was introduced in ES6, a major update to JavaScript, to solve this potential issue with the var keyword.If you replace var with let in the code above, it results in an error
e.g 
let camper = "James";

let camper = "David";

The error can be seen in your browser console,unlike var, when you use let, a variable with the same name can only be declared once.

We can also declare variables using the const,the declared using const are read only.Once the variable is assigned with const it cannot be reassigned
e.g
const FAV_PET = "Cats";

FAV_PET = "Dogs";

The console will display an error due to reassigning the value of FAV_PET.You should always name variables you don't want to reassign using the const keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant.

We are able to add two numbers using javascript.We use the + symbol as an operator when placed between two numbers.
e.g const sum = 10 + 10;

As we are able to add we also able to subtract
e.g const difference = 45 - 33

We are also able to multiply one number by another using the * symbol.
e.g const product = 8 * 10;

We can also divide one number by another using the / symbol
e.g const quotient = 66 / 33;

We can increment a number with javascript,we use the ++ operator to increment (i++) which is equivalent of i = i + 1;

We decrement a variable with the -- operator (i--) which is equivalent to i = i - 1;

We can store decimal numbers in variables too. Decimal numbers are sometimes referred to as floating point numbers or floats.
e.g const myDecimal = 5.7;


# Conclusion
I am going to continue with javascript.