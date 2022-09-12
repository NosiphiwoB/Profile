---
Layout:
Title: " Javascript Test 2"
Date: "2022 09 12"
---

# Introduction
Today I was busy with the javascript test.

# Body
Today Moral gave us test based on javascript 

1) Get the highest number in an array: 

const getHighestNumber = (array) =>{

return Math.max.apply(Math, array);

}

console.log(getHighestNumber([1, 3 , 10 , 12]))


2) Calculate sum in an array of objects:

const calculateSumOfList = (array) => {

  return array.map(item => item.score).reduce((prev, next) => prev + next);

}

console.log(calculateSumOfList([{score: 1 } ,{score: 2} ,{score: 5} , {score: 6} ,{score: 5}])) 


3) Remove an object based on id:

const removeObjectBasedOnId = (array , id) => {

    const removeObject = array.findIndex((remove) => remove.id === id);

    array.splice(removeObject, 1);
  
    return array;

}

console.log(removeObjectBasedOnId([{id:1 , name:'rocky'} , {id:2 , name:'smith'},{id:3 , name:'thabo'}] , 2)) 


4) Remove strings in an array:

const removeAllStrings = (array) => {

    let newArr = [ ];

    for (let i = 0; i < array.length; i ++) {

        !isNaN(array[i]) ? newArr.push(array[i]) : ''

    }

    return newArr

}

console.log(removeAllStrings(['b' , 11 , 'smith', 2 , 'van' , 88, 22])) 


6) Create an array based on Number:

const createArrayBasedOnNumber = (value) => {

let n = 11;

return Array.apply(null, {length: n}).map(Number.call, Number)

}

console.log(createArrayBasedOnNumber(11)) 


7) Add an Item at the beginning of an array:

const addItemBeginOfList = (array , value) => {

return array=([value, ...array])

}

console.log(addItemBeginOfList([2 , 4 , 6], 5)) 

# Conclusion
The test was good I just had a problem with one kata,I was not able solve:

const getTotalTwins = (array) => {

}

console.log(getTotalTwins([1 , 3 , 'b' , 'b' , 2 , 'w' , 1 , 1])) 

Im going to do a research on how to solve an array of numbers and letters.