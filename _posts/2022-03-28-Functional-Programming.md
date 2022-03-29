---
Layout:
Title: "Functional Programming"
Date: "2022 03 28"
---

# Introduction
Today I was with freecodecamp (Functional Programming).

# Body 
Return Part of an Array Using the slice Method, we use the slice method to return a copy of certain elements of an array.slice can take two arguments,the first gives the index of where to begin the slice and second is the index of where to end the slice.If there is no arguments provided te default is to start t the beginning of the array to the end.A slice method returns a new array.
 
 
Understand Functional Programming Terminology,Callbacks are the functions that are slipped or passed into another function to decide the invocation of that function.Functions that can be assigned to a variable, passed into another function, or returned from another function just like any other normal value, are called first class functions. In JavaScript, all functions are first class functions.The functions that take a function as an argument, or return a function as a return value are called higher order functions.When functions are passed in to or returned from another function, then those functions which were passed in or returned can be called a lambda.
e.g Prepare 27 cups of green tea and 13 cups of black tea and store them in tea4GreenTeamFCC and tea4BlackTeamFCC variables, respectively. Note that the getTea function has been modified so it now takes a function as the first argument : 
const prepareGreenTea = () => 'greenTea';
const prepareBlackTea = () => 'blackTea';
const getTea = (prepareTea, numOfCups) => {
const teaCups = [];
for(let cups = 1; cups <= numOfCups; cups += 1) {
    const teaCup = prepareTea();
    teaCups.push(teaCup);
  }
  return teaCups;
};
const tea4GreenTeamFCC = getTea(prepareGreenTea , 27); //answer
const tea4BlackTeamFCC = getTea(prepareBlackTea , 13); //answer .


Understand the Hazards of Using Imperative Code,an imperative style in programming is one that gives the computer a set of statements to perform a task.

# Conclusion
I am going to continue with javascript