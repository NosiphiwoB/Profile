---
Layout:
Title: "Debugging"
Date: "2022 03 15"
---

# Introduction
Today I was busy with debugging.

# Body
Debugging is the process of identifying and removing errors from the computer hardware or software.
To check the value of a variable we use Javascript console.We have different methods that can be used with console (log,warn,clear).freeCodeCamp console will only output log messages but the browser console will output all messages

Checking the Type of a Variable using typeof, we use typeof to check the data structure, or type, of a variable.
e.g Add two console.log() statements to check the typeof each of the two variables seven and three in the code:  
let seven = 7;
let three = "3";
console.log(typeof seven);
console.log(typeof three); .

Catch Unclosed Parentheses, Brackets, Braces and Quotes.We have to make sure that all opening parentheses, brackets,curly braces and quotes have a closing pair.We can avoid having unclosed  parentheses, brackets,curly braces and quotes by immediately including the closing match and move the cursor back between them and continue coding.

Catch Mixed Usage of Single and Double Quotes.javascript allows us to use both single quotes (') and double quotes (") to declare a string.If using one style of quotes we can escape the quotes inside the string by using the backslash (\) character.
e.g  const allSameQuotes = 'I\'ve had a perfectly wonderful evening, but this wasn\'t it.'; .

Catch Use of Assignment Operator Instead of Equality Operator, we use the equal to : assign a value to a variable (=),to check for equality we use (==) and (===).

Catch Missing Open and Closing Parenthesis After a Function Call,when calling a function we need to include the empty parentheses () even when it doesn't take any arguments.
e.g  function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}

let result = getNine();
console.log(getNine); .

Catch Arguments Passed in the Wrong Order When Calling a Function, it is important to make sure that you apply all required arguments in a proper order to avoid a runtime error.Having arguments that are different types  will throw a runtime  error.



# Conclusion
I am done with debugging,tomorrow will be moving on to the next coarse which is Basic Data Structures.
