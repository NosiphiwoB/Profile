---
Layout:
Title: "Functional Programming"
Date: "2022 03 30"
---


# Introduction
Today I aws busy with the remaining challenges on Functional Programming.

# Body
Sort an Array Alphabetically using the sort Method,sorth method sorts the elements of an array accordingg to the callback function.JavaScript's default sorting method is by string Unicode point value, which may return unexpected results. Therefore, it is encouraged to provide a callback function to specify how to sort the array items. 
.eg Use the sort method in the alphabeticalOrder function to sort the elements of arr in alphabetical order. The function should return the sorted array:
function alphabeticalOrder(arr) {

  return arr.sort() //answer

}
alphabeticalOrder(["a", "d", "c", "a", "z", "g"]); 

or function ascendingOrder(arr) {
  return arr.sort(function(a, b) {
    return a - b;
  });
}

alphabeticalOrder(["a", "d", "c", "a", "z", "g"]); .


Return a Sorted Array Without Changing the Original Array,sort method changes the order of the element in the original array.In order to avoid this we need to first concatenate an empty array to the one being sorted.
e.g Use the sort method in the nonMutatingSort function to sort the elements of an array in ascending order. The function should return a new array, and not mutate the globalArray variable:

const globalArray = [5, 6, 3, 2, 9];

function nonMutatingSort(arr) {

return [].concat(arr).sort(function(a,b) {

  return a - b;
  
});

}

nonMutatingSort(globalArray); .

Split a String into an Array Using the split Method,the split method splits a string into an array of strings.It takes an argument for the delimiter, which can be a character to use to break up the string or a regular expression. For example, if the delimiter is a space, you get an array of words, and if the delimiter is an empty string, you get an array of each character in the string.
e.g 
const str = "Hello World";

const bySpace = str.split(" ");

const otherString = "How9are7you2today";

const byDigits = otherString.split(/\d/);

bySpace would have the value ["Hello", "World"] and byDigits would have the value ["How", "are", "you", "today"].

Combine an Array into a String Using the join Method,join method joins the elements of an array together to create a string
e.g Use the join method (among others) inside the sentensify function to make a sentence from the words in the string str. The function should return a string. For example, I-like-Star-Wars would be converted to I like Star Wars. For this challenge, do not use the replace method:

function sentensify(str) {

return str.split(/\W/).join(" ");

}

sentensify("May-the-force-be-with-you");

# Conclusion
Tomorrow I will move on to the next course Intermediate Algorithm Scripting