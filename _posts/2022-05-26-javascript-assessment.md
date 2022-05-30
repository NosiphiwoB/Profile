---
Layout:
Title: "javaScript assessment"
Date: "2022 05 26"
---

# Introduction
Today I was busy with the javascript assessment

# Body
We were given a javascript which we were told not to use internet for answers.We had four questions to solve :

1)Given an array of names return the longest name.
e.g (['bob' , 'smith', 'longman']) longman. 
answer:

const getLongestName = () => {

    let array=["Noxolo","Akhona","Mondli","Kgotatso","Lehlokgonolo"];

    let longestName = " ";

    for(let i = 0; i < array.length; i++){

        if(array[i].length > longestName.length){

            longestName = array[i];

        }
    }

    return longestName;
}

console.log(getLongestName())


2)Given a function that passes two values value1 and value2 calculate the two values
and return the answer.
e.g (1 , 2) 3
answer :

function sum(a ,b){

    return a + b

}

console.log(sum(6,4))


3)given an array of values return the total amount.
e.g ([1 , 2 ,3 ]) 6
answer :

const calculateLIst = (a) =>{

   let numbers = [5,10,15,20,25,30,35,40];

  let sum = 0;

  for(let i = 0; i < numbers.length; i++){

      sum += numbers[i]

  }return sum

};

console.log(calculateLIst())


4)Given a value, you should be able to store the values in an array  
e.g [{name:"moral" , surname:"smith"} , {name:"thabo" , surname:"king"}] ["moral" , "thabo"]
answer :

function getNames(){

    let students = [

        {name:"Noxolo" , surname:"Biyela"},

        {name:"Akhona" , surname:"Shiceka"},

        {name:"Mondli" , surname:"Ndaba"},

        {name:"moral" , surname:"smith"}
    ]

    let newArray = [];

    for(let i = 0; i < students.length; i++){

        newArray.push(students[i].name);

        }

        return newArray

    }

console.log(getNames())


# Conclusion
I didn't have any issues with the assessment


