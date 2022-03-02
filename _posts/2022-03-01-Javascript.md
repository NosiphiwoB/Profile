---
Layout:
Title: "javascript"
Date: "2022 03 01"
---

# Introduction
Today I was busy with Javascript.

# Body
I learnt that we are able to update  the objects properties after you have created it.To update the object we use dot or bracket notation.
We also able to add properties to our object ,for an axample if we have  a dog as our object with name;legs;tails properties,we can add a bark property (ourDog.bark = "woof").
We  can also delete properties (delete ourDog.bark;).
We are able to access nested objects and arrays using dot or bracket notation.
We have loops,they used to run the same code multiple times
We have a while loop which runs while a specified condition is true and stops when the condition is no longer true.
There is also a for loop ,which runs for a specific number of times.
Nesting for loops,we are able to nest (have) a loop inside another loop.
e.g   const arr = [
  [1, 2], [3, 4], [5, 6]
];

for (let i = 0; i < arr.length; i++) {
  for (let j = 0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
We have Recursion whuch we can replace loops with,Recursion adds clarity and helps to reduce time needed to write and debug code.


# Conclusion
I am currently struggling with lookups,Testing Objects for Properties,manipulating complex objects.