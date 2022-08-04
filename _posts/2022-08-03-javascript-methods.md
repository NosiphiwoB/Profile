---
Layout:
Title: " JavaScript Methods"
Date: "2022 08 03"
---

# Introduction
Today we had a session with Tumisang,we discussed javascript methods.

# Body
We were not able to discuss all the methods due to time,but just to name the few that we discussed: 


1)push() - push method adds an item at the end of an array.

e.g cont list = ['juice','sweets','chips','meat','rice','milk'];

    let newList = list.push('sugar')

    console.log(list) ----> will return an array ['juice','sweets','chips','meat','rice','milk','sugar']


2)unshift() - unshift method adds an item at the beginning of an array.

e.g const list = ['juice','sweets','chips','meat','rice','milk'];

    let newList = list.unshift('sugar')

    console.log(list) ----> will return an array ['sugar','juice','sweets','chips','meat','rice','milk'];


3)pop() - pop method removes/deletes an item at the end of an array.

e.g const list = ['juice','sweets','chips','meat','rice','milk'];

    let newList = list.pop()

    console.log(list) ----> will return ['juice','sweets','chips','meat','rice'];


4)shift() - shift method removes/deletes an item at the beginning of an array.

e.g const list = ['juice','sweets','chips','meat','rice','milk'];

    let newList = list.shift()

    console.log(list) ----> will return ['sweets','chips','meat','rice','milk'];


sort() -The sort() method will sort elements based on the return value of the compare() function.

e.g const numbers = [0,3,4,7,9,5,8,1,6,2]

    let sortedNumbers = list.sort((a,b) => a - b)

This will return array sorted in an ascending order [0,1,2,3,4,5,6,7,8,9] 

    const numbers = [0,3,4,7,9,5,8,1,6,2]

    let sortedNumbers = list.sort((a,b) => b - a)

This will return array sorted in an desceding order [9,8,7,6,5,4,3,2,1,0] 


# Conclusion
I am going to continue practising the other javascript methods.I will also make time for the projects that I'm busy with.




