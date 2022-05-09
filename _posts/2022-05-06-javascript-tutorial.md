---
Layout:
Title: "Javascript Tutorials"
Date: "2022 05 06"
---

# Introduction
Today I was busy with javascript

# Body
I decided to do more practice on javascript methods and I also did a revision of what I have learnt since we started javascript tutorials.

<h5>1)slice()</h5>
slice method removes an item from an array and returns the removed items in an array , but it doesn't change the original array :

let students = ["Noxolo","Akhona","Mondli","Khathu","Feydo"];

let newStudents = students.slice(0,3)

console.log(newStudents) ---> will return ["Noxolo","Akhona","Mondli"]

console.log(students) ---> will return ["Noxolo","Akhona","Mondli","Khathu","Feydo"] --the origin array


<h5>2)splice()</h5>
slice method removes an item from an array  and return the removed items in an array,splice method changes the original array:

let students = ["Noxolo","Akhona","Mondli","Khathu","Feydo"];

let newStudents = students.splice(0,3)

console.log(newStudents) ---> will return [ "Noxolo","Akhona","Mondli" ]

console.log(students) ---> wil return ["Khathu","Feydo"]


<h5>3)toUpperCase()</h5>
toUpperCase method converts a string to upper case :

let name = "noxolo";

let newName = name.toUpperCase()

 console.log(newName) ---> will return "NOXOLO"


<h5>4)toLowerCase()</h5>
toLowerCase method converts a string to lower case:

let name = "NOXOLO";

let newName = name.toLowerCase()

console.log() ---> will return "noxolo"

<h5>5)Using toUpperCase and toLowerCase in one string</h5>
We are able to use both toUpperCase and toLowerCase in one string :

let name = "nOXOLO"

let newName = name[0].toUpperCase() + name.slice(1).toLowerCase();

console.log(newName) ---> will return "Noxolo"

# Conclusion
I will continue with javascript tutorials and also freecode camp.


