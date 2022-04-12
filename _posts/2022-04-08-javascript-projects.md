---
Layout:
Title: "javascript projects"
Date: "2022 04 08"
---


# Introduction
Today I was busy with telephone number validator and cash register.

# Body 
Telephone number validator is the process of checking if a phone number is accurate. It lets you find out if the phone number you have for a business contact or customer is active and able to receive calls.
e.g  function validatePhoneNumber(elementValue){

var phoneNumberPattern = /^\(?(\d{3})\)?[- ]?(\d{3})[- ]?(\d{4})$/;

return phoneNumberPattern.test(elementValue);

}

/^\(?: Means that the phone number may begin with an optional “(“.

(\d{3}): After the optional “(” there must be 3 numeric digits. If the phone number does not have a “(“, it must start with 3 digits. E.g. (308 or 308.
\)?: Means that the phone number can have an optional “)” after first 3 digits.
[- ]?: Next the phone number can have an optional hyphen (“-“) after “)” if present or after first 3 digits.
(\d{3}): Then there must be 3 more numeric digits. E.g (308)-135 or 308-135 or 308135
[- ]?: After the second set of 3 digits the phone number can have another optional hyphen (“-“). E.g (308)-135- or 308-135- or 308135-
(\d{4})$/: Finally, the phone number must end with four digits. E.g (308)-135-7895 or 308-135-7895 or 308135-7895 or 3081357895.

I was required to return true if the passed string looks like a valid US phone number.The user may fill out the form field any way they choose as long as it has the format of a valid US number,here is how I did it :

function telephoneCheck(str) {

 let rex1 = /^(1\s?)?\d{3}([-\s]?)\d{3}\2\d{4}$/,

        rex2 = /^(1\s?)?\(\d{3}\)\s?\d{3}[-\s]?\d{4}$/;

    if (rex1.test(str)) {

        return true;

    }

    else {

        return rex2.test(str) ? true : false

    }
}

telephoneCheck("555-555-5555"); .


I also did a cash register project,In this project I was required to design a cash register function that accepts purchase price as the first argument (price), payment as the second argument (cash), and cash-in-drawer (cid) as the third argument.

function checkCashRegister(price, cash, cid) {

  const INSUFFICIENT_FUNDS = {status: "INSUFFICIENT_FUNDS", change: []}

  const CLOSED = {status: "CLOSED", change: cid}

  const OPEN = {status: "OPEN", change: []}

  let totalCid = cidTotal();

  let dueBlance = parseFloat((cash - price).toFixed(2));

  if(totalCid < dueBlance) {

    return INSUFFICIENT_FUNDS;
  }

  if(totalCid === dueBlance) {

    return CLOSED;
  }

  let cashTypes = [

    ["ONE HUNDRED", 100],

    ["TWENTY", 20],

    ["TEN", 10],

    ["FIVE", 5],

    ["ONE", 1],

    ["QUARTER", 0.25],

    ["DIME", 0.1],

    ["NICKEL", 0.05],

    ["PENNY", 0.01],
  ];


  for(let i = 0; i < cashTypes.length; i++) {

    let cashType = cashTypes[i][0];

    let cashValue = cashTypes[i][1];

    let totalCash = cid.find(item => item[0] === cashType)[1];

    if(dueBlance > cashValue && dueBlance > totalCash ) { 

      dueBlance -= totalCash;

      OPEN.change.push([cashType, totalCash]);

    }else if(dueBlance > cashValue && totalCash > dueBlance) {

      let pay = Math.floor(dueBlance / cashValue) * cashValue;

      dueBlance -= pay;

      dueBlance = parseFloat(dueBlance.toFixed(2));

      OPEN.change.push([cashType, pay]);
    }
  }

  if(dueBlance > 0) {

    return INSUFFICIENT_FUNDS;
  }
  
  return OPEN;

  function cidTotal() {

    return parseFloat(cid.reduce((a,b) => a + b[1], 0).toFixed(2));
  }
}

# Conclusion
Since I am done with javascript I will be moving on to the next course.

