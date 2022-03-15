---
Layout:
Title: "REGULAR EXPRESSIONS PART I"
Date: "2022 03 11"
---

# Introduction
Today I was busy with REGULAR EXPRESSIONS.

# Body 
Regular expressions are patterns used to match character combination in strings.The patterns are used with the the exec() and test() methods of RegExp , and with the match() , matchAll() , replace() , replaceAll() , search() , and split() methods of String .

Using the Test Method. There .test() method takes the regex and applies it to a string that is placed inside the parentheses and return true or false if the pattern finds something or not.
e.g   let myString = "Hello, World!";
let myRegex = /Hello/;
let result = myRegex.test(myString);. The test method here will return true.

Match Literal Strings,we can also match literal string using .test().e.g  let waldoIsHiding = "Somewhere Waldo is hiding in this text.";
let waldoRegex = /Waldo/; 
let result = waldoRegex.test(waldoIsHiding);.There test will return true but /WALDO/ and Waldo will not match.

Matching a Literal String with Different Possibilities,we are able to search for multiple patterns using the alternation or the OR operator (|) .
e.g  let petString = "James has a pet cat.";
let petRegex = /dog|cat|bird|fish/; // Change this line
let result = petRegex.test(petString);

Ignoring Case While Matching,when matching we can ignore case by using the i-flag
e.g  let myString = "freeCodeCamp";
let fccRegex = /FREECodeCamp/i; 
let result = fccRegex.test(myString); . There result will be true due to the i-flag that was used.


Finding More Than the First Match,we can search a pattern more than once using the g-flag. 
e.g   let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /Twinkle/gi; 
let result = twinkleStar.match(starRegex);


Matching Anything with Wildcard Period, wildcard character (.) matches any one character.For an example if we want to match hug, huh, hut, and hum  we can use the regex /hu./ to match all the four words.

Matching Letters of the Alphabet, we have a hyphen (-) character that we use whn matching a large range of characters  
e.g  let catStr = "cat";
let batStr = "bat";
let matStr = "mat";
let bgRegex = /[a-e]at/;
catStr.match(bgRegex);
batStr.match(bgRegex);
matStr.match(bgRegex); .


# Conclusion
So far I don't have any issues with the challenges I have done so far.I am planning on finishing all the challenges on REGULAR EXPRESSIONS by Monday.