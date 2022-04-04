---
Layout:
Title: "Filter, Reduce, Map method"
Date: "2022 04 01"
---

# Introduction
Today I was busy with Filter, Reduce, Map method.

# Body
I am still struggling with this course Intermediate Algorithm Scripting,but I did go through some few things today (map, filter and reduce method).

I am going to start with a map method, the map() method creates a new array populated with the results of calling a provided function on every element in the calling array.We attach the map method to an array we want to iterate over.The map() function expects a callback as the argument and executes it once for each element in the array. From the callback parameters, you can access the current element, the current index, and the array itself.
For an example using the map method on the users array to return a new array containing only the names of the users as elements:

const users = [

  { name: 'John', age: 34 },

  { name: 'Amy', age: 20 },

  { name: 'camperCat', age: 10 }

];

const names = users.map(user => user.name);

console.log(names);

The console would display the value  [ 'John', 'Amy', 'camperCat' ].

The filter method,filter calls a function on each element of an array and returns a new array containing only the elements for which that function returns true,it filters the array, based on the function passed to it. Like map, it does this without needing to modify the original array.The callback function accepts three arguments. The first argument is the current element being processed. The second is the index of that element and the third is the array upon which the filter method was called.
For an example using the filter method on the users array to return a new array containing only the users under the age of 30. For simplicity, the example only uses the first argument of the callback :

const users = [

  { name: 'John', age: 34 },

  { name: 'Amy', age: 20 },

  { name: 'camperCat', age: 10 }

];

const usersUnder30 = users.filter(user => user.age < 30);

console.log(usersUnder30); 
 The console would display the value [{name: 'Amy', age: 20 }, { name: 'camperCat', age: 10}].

 Reduce method,with reduce you can filter and then map in a single pass.The reduce method iterates over each item in an array and returns a single value (i.e. string, number, object, array). This is achieved via a callback function that is called on each iteration.
 For an example using reduce on the users array to return the sum of all the users' ages. For simplicity, the example only uses the first and second arguments :
 const users = [
  { name: 'John', age: 34 },
  { name: 'Amy', age: 20 },
  { name: 'camperCat', age: 10 }
];

const sumOfAges = users.reduce((sum, user) => sum + user.age, 0);
console.log(sumOfAges);
The console would display the value 64.

const users = [
  { name: 'John', age: 34 },
  { name: 'Amy', age: 20 },
  { name: 'camperCat', age: 10 }
];

const usersObj = users.reduce((obj, user) => {
  obj[user.name] = user.age;
  return obj;
}, {});
console.log(usersObj);
The console would display the value { John: 34, Amy: 20, camperCat: 10 }

# Conclusion 
I am going to do the remaining challenges on Javascript and also do the projects.
