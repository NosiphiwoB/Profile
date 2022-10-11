---
Layout:
Title: " MongoDB and Mongoose "
Date: "2022 10 10"
---

# Introduction
Today I was busy with MongoDB and Mongoose.

# Body
Today I decided to read a mongoose article since I've been struggling with my repli.

Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.
MongoDB is a schema-less NoSQL document database.It means you can store JSON documents in it, and the structure of these documents can vary as it is not enforced like SQL databases. This is one of the advantages of using NoSQL as it speeds up application development and reduces the complexity of deployments.	

Creating a model --- We first need  a Schema.Each schema maps to a MongoDB collection.It defines the shape of the documents within that collection.Schema are building block for Models. They can be nested to create complex models. A model allows you to create instances of your objects called documents.Replit is a real server, and in real servers the interactions with the database happen in handler functions. These functions are executed when some event happens (e.g. someone hits an endpoint on your API). We’ll follow the same approach in these exercises. The done() function is a callback that tells us that we can proceed after completing an asynchronous operation such as inserting, searching, updating, or deleting. It's following the Node convention, and should be called as done(null, data) on success, or done(err) on error.

here is an example :

Create a person schema called personSchema having this prototype:

- Person Prototype -

--------------------

name : string [required]

age :  number

favoriteFoods : array of strings (*)


This is how you do it : 

mongoose.connect( mySecret, { useNewUrlParser: true, useUnifiedTopology: true });

const Schema = mongoose.Schema;

let Person;

const personSchema = new Schema({

  name: {type: String, required:true},

  age: Number,

  favoriteFoods: [String]

});

Person = mongoose.model("Person", personSchema);


# Conclusion
For now I don't have a clear understanding of how MongoDB and Mongoose works but I will continue with the challlenges.