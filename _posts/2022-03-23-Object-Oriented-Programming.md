---
Layout:
Title: "Object Oriented Programming"
Date: "2022 03 23"
---

# Introduction
Today I  was busy with Object Oriented Programming.Object Oriented Programming,is one of the major approaches to the software development process. In Object Oriented Programming objects and classes organize code to describe things and what they can do.


# Body
We use dot notation to access the properties of an object ,we are able to access as many properties as we want.
e.g let dog = {
  name: "Spot",
  numLegs: 4,
  tails: 1
};
console.log(dog.name,dog.numLegs,dog.tails)

Creating a Method on an Object.Methods adds different behavior to a object,they are properties that are functions.
e.g let dog = {
  name: "Spot",
  numLegs: 4,
sayLegs: function() {return "This dog has " + dog.numLegs + " legs.";}
};


Making Code More Reusable with the this Keyword,when using a dot notation if a variable name changes any code referencing the name would need to be updated as well.To avoid these issues we can use the (this) keyword.
e.g let dog = {
  name: "Spot",
  numLegs: 4,
  sayLegs: function() {return "This dog has " + this.numLegs + " legs.";}
};

Defining a Constructor Function, constructors creates new objects (this inside the constructor always refers to the object being created).They define  properties and behaviors that will belong to the new object.Constructors follow a few conventions:
Constructors are defined with a capitalized name to distinguish them from other functions that are not constructors.
Constructors use the keyword this to set properties of the object they will create.
Constructors define properties and behaviors instead of returning a value as other functions might.
e.g function Dog() {
  this.name = "Bobby";
  this.color = "white";
  this.numLegs = 4;
} .

Create Objects Using a Constructor, we use the new operator when calling a constructor.new operator tells javascript to create  a new object.
e.g function Bird() {
  this.name = "Albert";
  this.color  = "blue";
  this.numLegs = 2;
}

let blueBird = new Bird();  .

Extend Constructors to Receive Arguments,designing your Dog constructor to accept parameters makes it easy to create different Dog object
e.g  function Dog(name, color) {
  this.name = name;
  this.color = color;
  this.numLegs = 4;
}
let terrier = new Dog(); .

Verify an Object's Constructor with instanceof, new objects created with a constructor function are said to be an  instance of its constructor.We compare an object to a constructor using instanceof,result will return true or false depending on whether or not the object was created with the constructor
e.g  let Bird = function(name, color) {
  this.name = name;
  this.color = color;
  this.numLegs = 2;
}

let crow = new Bird("Alexis", "black");

crow instanceof Bird; .

Understand Own Properties, own properties are defined directly on the instance object.
e.g function Bird(name) {
  this.name = name;
  this.numLegs = 2;
}
let duck = new Bird("Donald");
let canary = new Bird("Tweety"); , name and numLeg are called own properties.

# Conclusion
Tomorrow I will be finishing the remaining challenges on  Object Oriented Programming and also continue with my To do list project.