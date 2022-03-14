---
Layout:
Title: "REGULAR EXPRESSIONS"
Date: "2022 03 14"
---

# Introduction
 Today I was busy with regular expression and I managed to finish all the challenges on regular expression..

 # Body
 Matching Numbers and Letters of the Alphabet,we can also match numbers  using the hyphen character.It is also possible to combine a range of letters and numbers is a single character set
e.g  let quoteSample = "Blueberry 3.141592653s are delicious.";
let myRegex = /[h-s2-6]/gi; 
let result = quoteSample.match(myRegex); 


Matching Single Characters Not Specified,we have negated character sets which are set of characters that do not match.To create a negated character sets we place a caret character (^) after opening a bracket and before the characters we don't want to match 
e.g let quoteSample = "3 blind mice.";
let myRegex = /[^aeiou0-9]/gi; 
let result = quoteSample.match(myRegex); .
We also use the caret character to search for patterns at the beginning of string
e.g  let rickyAndCal = "Cal and Ricky both like racing.";
let calRegex = /^Cal/; 
let result = calRegex.test(rickyAndCal); .

Match Characters that Occur One or More Times,to check if the character occurs once or repeated we use the (+) character 
e.g If we want to find matches when the letter (s) occurs one or more times in Mississippi : let difficultSpelling = "Mississippi";
let myRegex = /s+/gi; 
let result = difficultSpelling.match(myRegex);
To match characters that occurs zero or more times  we use the star (*) character 

Lazy Matching,finds the smallest  possible part of the string that satifies the regex pattern.Lazy matching uses (?) character
e.g  let text = "<h1>Winter is coming</h1>";
let myRegex = /<.*?>/;
let result = text.match(myRegex); ,this will return the HTML tag <h1> and not the text "<h1>Winter is coming</h1>".

Matching Ending String Patterns,we search for patterns at the end of the string using the dollar sign ($) at the end of the regex.
e.g  let caboose = "The last car on a train is the caboose";
let lastRegex = /caboose$/; 
let result = lastRegex.test(caboose); .


Matching All Letters and Numbers, we have a shortcut to match alphabet (\w) which is equal to [A-Za-z0-9_]. The \w characters matches upper and lowercase , numbers and the underscore character.


Matching Everything But Letters and Numbers, we have the opposite of \w which is \W .\W is a shortcut for [^A-Za-z0-9_] . It matches the non-alphanumeric characters.
We can also search for just digits or numbers using the \d character which is equal to the character class [0-9].
e.g  let movieName = "2001: A Space Odyssey";
let numRegex = /\d/g; 
let result = movieName.match(numRegex).length;  .
To search for non-numbers we use the character \D which is equal to [^0-9] .

Matching Whitespace, we search for whitespace using the \s.This pattern not only matches whitespace, but also carriage return, tab, form feed, and new line characters which is equal to character class [ \r\t\f\n\v] . 
e.g let whiteSpace = "Whitespace. Whitespace everywhere!"
let spaceRegex = /\s/g;
whiteSpace.match(spaceRegex); ,this will return [" ", " "]. 
We can also search for non-whitespace using \S.The pattern will not match whitespace,carriage return, tab, form feed, and new line characters.\S is similar to character class [^ \r\t\f\n\v] .

Specify Upper and Lower Number of Matches,we have quantity specifiers ({}) which specifies the lower and upper number of pattern
e.g To match the entire phrase Oh no only when it has 3 to 6 letter h's : 
let ohStr = "Ohhh no";
let ohRegex = /Oh{3,6} no/; 
let result = ohRegex.test(ohStr);. 
We can also specify Only the Lower Number of Matches
e.g To match the word Hazzah only when it has four or more letter z's : 
let haStr = "Hazzzzah";
let haRegex = /Haz{4,}ah/; 
let result = haRegex.test(haStr); .


Specify Exact Number of Matches, to specify a certain number of patterns, just have that one number between the curly brackets.
e.g  let timStr = "Timmmmber";
let timRegex = /Tim{4}ber/;
let result = timRegex.test(timStr);

Check for All or None,we can specify the possible existence of an element with a question mark, ?
e.g let american = "color";
let british = "colour";
let rainbowRegex= /colou?r/;
rainbowRegex.test(american);
rainbowRegex.test(british); , both will return true.

Positive and Negative Lookahead, lookaheads can be used when we want to search  for multiple patterns over the same string.A positive  lookahead     (?=...) will look to make sure the element in the search pattern is there,but won't actually match it.A negative lookahead (?!...) will look to make sure the element in the search pattern is not there.
e.g  matching passwords that are greater than 5 characters long, and have two consecutive digits: let sampleWord = "astronaut";
let pwRegex = /(?=\w{6})(?=\w*\d{2})/;
let result = pwRegex.test(sampleWord);
 
 # Conclusion 
 Tomorrow will be moving on to the next course (Debugging).So far I don't have any problems on regular expression.