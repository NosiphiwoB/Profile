---
Layout:
Title: "Functional Programming"
Date: "2022 03 24"
---

# Introduction
Today I was busy with Functional Programming.Functional programming is another approach to software development.code is organized into smaller, basic functions that can be combined to build complex programs.It is a style of programming where solutions are simple, isolated functions, without any side effects outside of the function scope: INPUT -> PROCESS -> OUTPUT.Functional programming is about isolated functions meaning there is no dependence on the state of the program,pure functions (the same inpute always gives the same output), and Functions with limited side effects - any changes, or mutations, to the state of the program outside the function are carefully controlled.

# Body
Use Prototype Properties to Reduce Duplicate Code,to avoid duplicate code we use prototype.Properties in the prototype are shared among all instances of Bird(our example).
e.g function Bird(name) {
  this.name = name;
}
Bird.prototype.numLegs = 2; .

Iterate Over All Properties,we have two kinds of properties (own properties and prototype properties).Own properties are defined directly on the object instance itself. And prototype properties are defined on the prototype.

Understand the Constructor Property.The advantage of the constructor property is that it's possible to check for this property to find out what kind of object it is
e.g function joinBirdFraternity(candidate) {
  if (candidate.constructor === Bird) {
    return true;
  } else {
    return false;
  }
} . It’s generally better to use the instanceof method to check the type of an object.

Change the Prototype to a New Object,we able to set the prototype to a new object that already contains the properties,the properties are  added all at once
e.g Bird.prototype = {
  numLegs: 2, 
  eat: function() {
    console.log("nom nom nom");
  },
  describe: function() {
    console.log("My name is " + this.name);
  }
}; . When ever a prototype is manually  set to a new object, we also need define the constructor property.
e.g Bird.prototype = {
  constructor: Bird,
  numLegs: 2,
  eat: function() {
    console.log("nom nom nom");
  },
  describe: function() {
    console.log("My name is " + this.name); 
  }
}; .


# Conclusion
Tomorrow I will be busy with y To do list project,once I am done with it I am going to continue with freecodecamp.