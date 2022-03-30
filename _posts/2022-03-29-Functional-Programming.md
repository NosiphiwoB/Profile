---
Layout:
Title: "Functional Programming"
Date: "2022 03 29"
---

# Introduction
I am still busy with javascript Functional Programming.

# Body
Remove Elements from an Array Using slice Instead of splice,splice method takes arguments for the index of where to start removing items, then the number of items to remove.If the second argument is not provided, the default is to remove items through the end.The slice method does not mutate the original array, but returns a new one which can be saved into a variable.

e.g Rewrite the function nonMutatingSplice by using slice instead of splice. It should limit the provided cities array to a length of 3, and return a new array with only the first three items:

function nonMutatingSplice(cities) {

 return cities.slice(inputCities, 3);
 
} .

Combine Two Arrays Using the concat Method,Concatenation means to join items end to end.We can concat both strings and arrays.For arrays, the method is called on one, then another array is provided as the argument to concat, which is added to the end of the first array. It returns a new array and does not mutate either of the original arrays.
e.g Use the concat method in the nonMutatingConcat function to concatenate attach to the end of original. The function should return the concatenated array :

function nonMutatingConcat(original, attach) {

return original.concat(attach); //answer

}

const first = [1, 2, 3];

const second = [4, 5];

nonMutatingConcat(first, second); .

Add Elements to the End of an Array Using concat Instead of push, we can also use concat to add an item to the end of the same array.
e.g
 function nonMutatingPush(original, newItem) {

  return original.concat(newItem); //answer

}

const first = [1, 2, 3];

const second = [4, 5];

nonMutatingPush(first, second); .

Use the reduce Method to Analyze Data.The reduce method iterates over each item in an array and returns a single value (i.e. string, number, object, array). This is achieved via a callback function that is called on each iteration.The callback function accepts four arguments,the first is the accumultor (gets assigned the return value of the callback function from the previous iteration,the second is the current element being processed, the third is the index of that element and the fourth is the array upon which reduce is called.
 e.g  const users = [
 
  { name: 'John', age: 34 },
  
  { name: 'Amy', age: 20 },
  
  { name: 'camperCat', age: 10 }
  
];

const usersObj = users.reduce((obj, user) => {

  obj[user.name] = user.age;
  return obj;
  
}, {});

console.log(usersObj); .

# Conclusion
I am struggling with the whole Functional Programming course,so I am going to watch some youtube tutorials for a better understanding.