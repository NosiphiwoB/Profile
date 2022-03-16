---
Layout:
Title: "Basic Data Structures"
Date: "2022 03 16"
---

# Introduction
Today I was busy with the Basic Data Structures.

# Body
Access an Array's Contents Using Bracket Notation, we can retrieve an element from an array by enclosing an index in brackets nd append it to the end of ana array or to a variable which references an array object.


Add Items to an Array with push() and unshift(), we have a push() and unshift()  methods which can be used to modify an array.both methods can take one or more elements as parameters and add them to the array.The push() method adds to the end of an array.The unshift() adds to the beginning
e.g We have defined a function, mixedNumbers, which we are passing an array as an argument. Modify the function by using push() and unshift() to add 'I', 2, 'three' to the beginning of the array and 7, 'VIII', 9 to the end so that the returned array contains representations of the numbers 1-9 in order  : function mixedNumbers(arr) {
  arr.unshift("I" , 2 ,"three");
  arr.push(7, "VIII" , 9);
  return arr;
} .

Remove Items from an Array with pop() and shift().The pop() method removes an element from the end of an array, the shift() method removes an element fromthe beginning of an array
e.g We have defined a function, popShift, which takes an array as an argument and returns a new array. Modify the function, using pop() and shift(), to remove the first and last elements of the argument array, and assign the removed elements to their corresponding variables, so that the returned array contains their values : 
function popShift(arr) {
  let popped = arr.pop(); 
  let shifted = arr.shift(); 
  return [shifted, popped];
} .

Remove Items Using splice(), we use splice() method if we want to remove an element in the middle or if we want to remove more than one element at once.splice() can take up to 3 parameters.There first two parameters are integers which represent indexes , or positions of the array that splice is being called upon. The arrays are zero-indexed meaning the first element of an array is 0.splice() also returns a new array contatianing the value of the removed elements. 
e.g We've initialized an array arr. Use splice() to remove elements from arr, so that it only contains elements that sum to the value of 10 : 
const arr = [2, 4, 5, 1, 7, 5, 2, 1];
arr.splice(1,4)
console.log(arr); .

The third parameter of splice() adds to the array.
e.g We have defined a function, htmlColorNames, which takes an array of HTML colors as an argument. Modify the function using splice() to remove the first two elements of the array and add 'DarkSalmon' and 'BlanchedAlmond' in their respective places : 
function htmlColorNames(arr) {
arr.splice(0, 2, 'DarkSalmon', 'BlanchedAlmond')
  return arr;
} . 

Copy Array Items Using slice(), slice() copies or extracts a given number of elements to a new array,leaving an array it is called upon untouched.splice takes only 2 parameters.The first parameter is the index at which to begin extraction and the second is the index at which to stop extraction (but will not include the element at this element).
e.g We have defined a function, forecast, that takes an array as an argument. Modify the function using slice() to extract information from the argument array and return a new array that contains the string elements warm and sunny :
function forecast(arr) {
  return arr.slice(2,4);
}

Copy an Array with the Spread Operator, spread operator allows us to copy all of an array. Spread operator looks like this (...) .
e.g We have defined a function, copyMachine which takes arr (an array) and num (a number) as arguments. The function is supposed to return a new array made up of num copies of arr. We have done most of the work for you, but it doesn't work quite right yet. Modify the function using spread syntax so that it works correctly (hint: another method we have already covered might come in handy here!) : 
function copyMachine(arr, num) {
  let newArr = [];
  while (num >= 1) {
newArr.push([...arr])
    num--;
  }
  return newArr;
} .

We can also combine arrays or insert all the elements of one array into another array at any index with the spread operator
e.g We have defined a function spreadOut that returns the variable sentence. Modify the function using the spread operator so that it returns the array ['learning', 'to', 'code', 'is', 'fun'] :
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ["learning", ...fragment, "is", "fun"]; 
    return sentence;
} .

Check For The Presence of an Element With indexOf(), indexOf() allows us to check for the presence of an element on an array.indexOf() takes an element as a parameter, and when called, it returns the position, or index, of that element, or -1 if the element does not exist on the array.
e.g indexOf() can be incredibly useful for quickly checking for the presence of an element on an array. We have defined a function, quickCheck, that takes an array and an element as arguments. Modify the function using indexOf() so that it returns true if the passed element exists on the array, and false if it does not : 
function quickCheck(arr, elem) {
if (arr.indexOf(elem) >= 0) {
    return true;
  }
  return false;
} .

Add Key-Value Pairs to JavaScript Objects, we can add key-values to javascript object
e.g A foods object has been created with three entries. Using the syntax of your choice, add three more entries to it: bananas with a value of 13, grapes with a value of 35, and strawberries with a value of 27 :
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
};
foods['bananas'] = 13,
foods['grapes'] = 35,
foods['strawberries'] =27

# Conclusion
I managed to finish the challenges in this course.Tomorrow I will be starting a Basic Algorithm Scripting course.