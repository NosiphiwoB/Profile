---
Layout:
Title: " React Practise"
Date: "2022 10 19"
---

# Introduction
Today I was with react practise.

# Body
So today I basically doing the form test again just to see if I understand what I have done so far.

I also did one challenge on freecode camp.The reason why I did one it's because of the Replit,it is giving me problem.
The challlenge that I did was creating many records with model.create() --Sometimes you need to create many instances of your models, e.g. when seeding a database with initial data. Model.create() takes an array of objects like [{name: 'John', ...}, {...}, ...] as the first argument, and saves them all in the db.

e.g Modify the createManyPeople function to create many people using Model.create() with the argument arrayOfPeople :

const mongoose = require('mongoose');
mongoose.connect(process.env.MONGO_URI);

var personSchema = new mongoose.Schema({
  name: String,
  age: Number,
  favoriteFoods: [String]
});

var Person = mongoose.model('Person', personSchema);

var createAndSavePerson = function(done) {
  var janeFonda = new Person({name: "Jane Fonda", age: 84, favoriteFoods: ["eggs", "fish", "fresh fruit"]});

  janeFonda.save(function(err, data) {
    if (err) return console.error(err);
    done(null, data)
  });
};

var arrayOfPeople = [
  {name: "Frankie", age: 74, favoriteFoods: ["Del Taco"]},
  {name: "Sol", age: 76, favoriteFoods: ["roast chicken"]},
  {name: "Robert", age: 78, favoriteFoods: ["wine"]}
];

var createManyPeople = function(arrayOfPeople, done) {
  Person.create(arrayOfPeople, function (err, people) {
    if (err) return console.log(err);
    done(null, people);
  });
};

# Conclusion
I am going to continue with freecode camp and also do more practise .