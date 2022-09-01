---
Layout:
Title: " Javascript Test"
Date: "2022 08 31"
---


# Introduction
Today I was busy with the javascript test.

# Body

var groceryList = [{name:'hfhg', price:20 , quantity: 2}]

var total= 0

// Create a function that adds to groceryList:

const addToGroceryList = (item) => {

   groceryList.push(item)

};

console.log("adding to groceryList",addToGroceryList({name:'Pap', price:20 , quantity: 1}))

console.log("added item",groceryList)

// Create a function that removes items based on index groceryList:

const removeBasedOnIndex = (index) => {

    // console.log('index', index)

  return groceryList.splice(index ,1) 

}

console.log("rem",removeBasedOnIndex(0))

console.log("removed item",groceryList)

// output: groceryList must be [{name:'Pap', price:20 , quantity: 1}]


// Create a function to calculate the total price of items based on price and quantity:

const calculateTotal = () => {

for (let i in groceryList) {

    total += groceryList[i].price * groceryList[i].quantity
    
    return total

}

}

// function must return 20

console.log(calculateTotal())

// console.log(groceryList)

# Conclusion
I am going to continue with d3 projects and javascript.