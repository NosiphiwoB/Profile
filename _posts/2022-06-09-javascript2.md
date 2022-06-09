---
Layout:
Title: "javaScript assessment 2"
Date: "2022 06 09"
---

# Introduction
Today I was busy with the javascript assessment two.

# Body
I created four functions
1)Function that returns average mark.
2)Function that edits the name.
3)Function that get a total in a string.
4)Function that removes non numbers in a string.

You can use console.log in the terminal to check for the outcome:

const classMarks = [{name:"Thabo", mark:40},{name:"Smith", mark:33},{name:"Nean", mark:22}];

// function that calculates the average

function getAvg(classMarks) {

    const total=95;

    for(let i = 0; i < classMarks.length; i++)

    return total / classMarks.length;

  }

  const average = getAvg(classMarks);

  console.log(average);


// function that edits name

const editName = (arr, position, str) => {

    arr[position - 1].name = str;

    return arr;

  };

  console.log(editName(classMarks, 3, "Kagiso"));

//   function that gets total string

const getTotalString = (str) => {

    let string = 0;

    let number = /[0-9]/g;

    let newString = str.match(number);

    let sum = newString.map((x) => Number(x));

    for (let i = 0; i < sum.length; i++) {

      string += sum[i];

    }

    return string;

  };

  console.log(getTotalString("4T354B3434234234234"));


// function that returns numbers

  let arr = ["5", "g", 3, 5, 10, "dfdfdf"];

 const removeNonNumbers = (array) => {

  let newArray = [];

  let num = array.map((x) => Number(x));

  let num2 = num.map((j) => j.toString());

  for (let i = 0; i < num2.length; i++) {

    if (num2[i] != "NaN") {

      newArray.push(num2[i]);

    }

  }

  return newArray.map((y) => Number(y));

};

console.log(removeNonNumbers(arr));

# Conclusion
The assessment was a bit challenging and that made me realise that I need to try and practise on the monthly basis.