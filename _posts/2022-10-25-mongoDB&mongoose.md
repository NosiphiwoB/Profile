---
Layout:
Title: " MongoDB and Mongoose "
Date: "2022 10 25"
---



# Introduction
Today I was busy with freecode camp (MongoDB and Mongoose).I  am only left with one challenge on MongoDB and Mongoose than I will start with the projects.

# Body
Use model.find() to search your database -- Model.find() accepts a query document (a JSON object) as the first argument, then a callback. It returns an array of matches. It supports an extremely wide range of search options. Read more in the docs.

Modify the findPeopleByName function to find all the people having a given name, using Model.find() -> [Person].Use the function argument personName as the search key:

const findPeopleByName = (personName, done) => {

  Person.find({name: personName}, function (err, personFound){ 

    if(err) return console.log(err)   

  done(null, personFound);  

    });    

};



Use model.findOne() to Return a Single Matching Document from Your Database -- Returns only one document (not an array), even if there are multiple items. It is especially useful when searching by properties that you have declared as unique.

e.g Modify the findOneByFood function to find just one person which has a certain food in the person's favorites, using Model.findOne() -> Person. Use the function argument food as search key: 

var findOneByFood = function(food, done) {

  Person.findOne({favoriteFoods: food}, function (err, data) {

    if (err) return console.log(err);

    done(null, data);

  });

};



Use model.findById() to Search Your Database By _id -- When saving a document, MongoDB automatically adds the field _id, and set it to a unique alphanumeric key. Searching by _id is an extremely frequent operation, so Mongoose provides a dedicated method for it.

e.g Modify the findPersonById to find the only person having a given _id, using Model.findById() -> Person. Use the function argument personId as the search key:

const findPersonById = (personId, done) => {

  Person.findById(personId, function (err,personFound){

    if(err) return console.log(err)

  done(null, personFound);

  });

};


Perform Classic Updates by Running Find, Edit, then Save --- this was what you needed to do if you wanted to edit a document, and be able to use it somehow (e.g. sending it back in a server response). Mongoose has a dedicated updating method: Model.update(). It is bound to the low-level mongo driver. It can bulk-edit many documents matching certain criteria, but it doesn’t send back the updated document, only a 'status' message. Furthermore, it makes model validations difficult, because it just directly calls the mongo driver.

e.g const findEditThenSave = (personId, done) => {

   const foodToAdd = 'hamburger';

  Person.findById(personId, (err, person) => {

    if(err) return console.log(err); 

    person.favoriteFoods.push(foodToAdd);

    person.save((err, updatedPerson) => {

      if(err) return console.log(err);

      done(null, updatedPerson)

    })

  })

};



Perform New Updates on a Document Using model.findOneAndUpdate() --- Recent versions of Mongoose have methods to simplify documents updating. Some more advanced features (i.e. pre/post hooks, validation) behave differently with this approach, so the classic method is still useful in many situations. findByIdAndUpdate() can be used when searching by id .

e.g Modify the findAndUpdate function to find a person by Name and set the person's age to 20. Use the function parameter personName as the search key.You should return the updated document. To do that, you need to pass the options document { new: true } as the 3rd argument to findOneAndUpdate(). By default, these methods return the unmodified object:

const findAndUpdate = (personName, done) => {

  const ageToSet = 20;

  Person.findOneAndUpdate({name: personName}, {age: ageToSet}, {new: true}, (err, updatedDoc) => {

    if(err) return console.log(err);

    done(null, updatedDoc);

  })

};



Delete One Document Using model.findByIdAndRemove --- findByIdAndRemove and findOneAndRemove are like the previous update methods. They pass the removed document to the db. As usual, use the function argument personId as the search key:

const removeById = function(personId, done) {

  Person.findByIdAndRemove(

    personId,

    (err, removedDoc) => {

      if(err) return console.log(err);

      done(null, removedDoc);

    }

  ); 

};


Delete Many Documents with model.remove() -- Modify the removeManyPeople function to delete all the people whose name is within the variable nameToRemove, using Model.remove(). Pass it to a query document with the name field set, and a callback.

e.g const removeManyPeople = (done) => {

  const nameToRemove = "Mary";

  Person.remove({name: nameToRemove}, (err, response) => {

    if(err) return console.log(err);

    done(null, response);

  })

};


# Conclusion
For now I am going to continue with freecode camp.