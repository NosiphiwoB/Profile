---
Layout:
Title: "Basic Algorithm Scripting"
Date: "2022 03 17"
---

# Introduction
Today I was busy with Basic Algorithm Scripting and To do list  project.

# Body
Convert Celsius to Fahrenheit, the algorithm to convert from Celsius to Fahrenheit is the temperature in Celsius times 9/5, plus 32
e.g Use the variable fahrenheit already defined and assign it the Fahrenheit temperature equivalent to the given Celsius temperature. Use the algorithm mentioned above to help convert the Celsius temperature to Fahrenheit :
function convertToF(celsius) {
  let fahrenheit = celsius * 9 / 5 + 32;
  return fahrenheit;
} .

Reverse a String,reversing a string would be useful for debugging,it can also be an alternative way to write the loop.
Here is an example: 
function reverseString(str) {
 return str.split("").reverse().join(""); //changed this line
}

reverseString("hello"); .

Factorialize a Number, factorial is a function that multiplies a number by everynumber below it e.g 5!= 5*4*3*2*1=120 .

Find the Longest Word in a String , 



 let words = str.split(' ');
  let maxLength = 0;

  for (let i = 0; i < words.length; i++) {
    if (words[i].length > maxLength) {
      maxLength = words[i].length;
    }
  }

  return maxLength;
}


I also started with the TO DO LIST project that was given by Moral.The to do list must have the following : 
Subject,Description,Date picker and a Submit button.
After clicking submit button the information submited must show on table below.The table must have edit and delete  button.
So far this is what I have managed to do :
https://github.com/NosiphiwoB/To-do-list

# Conclusion
As much as I was able to finish all the challenges I am realy struggling with Basic Algorithm Scripting.I am planning to watch some you tube tutorials.
