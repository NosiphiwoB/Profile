---
Layout:
Title: "Javascript Projects"
Date: "2022 04 06"
---

# Introduction
Today I was busy with Javascript projects

# Body
I managed to do two javascript projects:

1) Roman numeral converter,I had to convert the given number into a roman numeral. All roman numerals answers should be provided in upper-case

Here is how I converted the numbers

function convertToRoman(num) {

   if (isNaN(num))

        return NaN;

    var digits = String(+num).split(""),

        key = ["","C","CC","CCC","CD","D","DC","DCC","DCCC","CM",

               "","X","XX","XXX","XL","L","LX","LXX","LXXX","XC",

               "","I","II","III","IV","V","VI","VII","VIII","IX"],

        roman = "",

        i = 3;

    while (i--)

        roman = (key[+digits.pop() + (i * 10)] || "") + roman;

    return Array(+digits.join("") + 1).join("M") + roman;
}

convertToRoman(36);

2) The second project that I did was Caesars Cipher,I had to write a function which takes a ROT13 enconded string as an input and returns a decoded string.ROT13 (rotate number by 13) means each letter subtituted  with the 13th letter after it in the alphabet

function rot13(str) {

let newStr = "";

  for(let i = 0; i < str.length; i++) {

    newStr += shiftLetter(str[i], 13);

  }

  return newStr;

}

function shiftLetter(l, s) {

  l = l.toUpperCase();

  const alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";

  let newInd = (alphabet.indexOf(l)+s)%26;

  return alphabet.includes(l) ? alphabet[newInd] : l; 
}

I also did a tribute page project using html and css,this is a project that I have done before but I felt like I needed to redo it and add some few things to make it look good
Here is the link for my tribute page project : https://nosiphiwob.github.io/Tribute-page/


# Conclusion
I am going to finish the remaining projects on javascript and also re-do the other projects that I did on codepen.I am also planning on watching javascript crash course because I am really struggling when it comes to javascript.