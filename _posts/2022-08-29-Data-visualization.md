---
Layout:
Title: " Data Visuliazation"
Date: "2022 08 29"
---

# Introduction
Today I was busy data visualization.I am only left with five challenges to finish 3d and start with my projects.

# Body
APIs are tools that computers use to communicate with one another, in part to send and receive data.
Programmers often use AJAX (Asynchronous JavaScript and XML) when working with APIs. AJAX refers to a group of technologies that make asynchronous requests to a server to transfer data, then load any returned data into the page. And the data transferred between the browser and server is often in a format called JSON (JavaScript Object Notation).


If you want your code to execute only once your page has finished loading ,you can attach  a javascript event to the document called  DOMContentLoaded :

document.addEventListener('DOMContentLoaded', function() {

});

We can implement event handlers that go inside of the DOMContentLoaded function.We can implement an onclick event handler which triggers when the user click on the element with id getMessage :

document.getElementById('getMessage').onclick = function(){};

e.g Add a click event handler inside of the DOMContentLoaded function for the element with id of getMessage:

 document.addEventListener('DOMContentLoaded', function(){

    document.getElementById("getMessage").onclick = function(){

    }

  });

When the click event happens, you can use JavaScript to update an HTML element.For example, when a user clicks the Get Message button, it changes the text of the element with the class message to say Here is the message :

document.getElementsByClassName('message')[0].textContent="Here is the message";

e.g Add code inside the onclick event handler to change the text inside the message element to say Here is the message :

 document.addEventListener('DOMContentLoaded', function(){

    document.getElementById('getMessage').onclick = function(){

      // Add your code below this line

   document.getElementsByClassName('message')[0].textContent="Here is the message";

      // Add your code above this line

    }

  });
  
You can also request data from external source using APIs.APIs - or Application Programming Interfaces - are tools that computers use to communicate with one another.Most web APIs trasfer data in a format called JSON .JSON stands for Javascript Object Notation.JSON syntax looks very similar to JavaScript object literal notation. JSON has object properties and their current values, sandwiched between a { and a }.

The JSON.parse method parses the string and constructs the JavaScript object described by it.

e.g document.addEventListener('DOMContentLoaded', function(){

    document.getElementById('getMessage').onclick = function(){

      // Add your code below this line

  const req = new XMLHttpRequest();

   req.open("GET",'/json/cats.json',true);

   req.send();

   req.onload = function(){

     const json = JSON.parse(req.responseText);

     document.getElementsByClassName('message')[0].innerHTML = JSON.stringify(json)

   };

      // Add your code above this line

    };

  });
  
The JavaScript XMLHttpRequest object has a number of properties and methods that are used to transfer data. First, an instance of the XMLHttpRequest object is created and saved in the req variable. Next, the open method initializes a request - this example is requesting data from an API, therefore is a GET request. The second argument for open is the URL of the API you are requesting data from. The third argument is a Boolean value where true makes it an asynchronous request. The send method sends the request. Finally, the onload event handler parses the returned data and applies the JSON.stringify method to convert the JavaScript object into a string. This string is then inserted as the message text.

We can also request external  data using  the javascript fetch() method,which is equivalent to XMLHttpRequest.

e.g document.addEventListener('DOMContentLoaded',function(){

    document.getElementById('getMessage').onclick= () => {

      // Add your code below this line

    fetch('/json/cats.json')

       .then(response => response.json())

       .then(data => {

         document.getElementById('message').innerHTML = JSON.stringify(data);

       })

      // Add your code above this line  

    };

The first line is the one that makes the request. So, fetch(URL) makes a GET request to the URL specified. The method returns a Promise.

After a Promise is returned, if the request was successful, the then method is executed, which takes the response and converts it to JSON format.

The then method also returns a Promise, which is handled by the next then method. The argument in the second then is the JSON object you are looking for!

Now, it selects the element that will receive the data by using document.getElementById(). Then it modifies the HTML code of the element by inserting a string created from the JSON object returned from the request.


Accessing the the JSON data from an API.Arrays use bracket notation to access a specific index of an item. Objects use either bracket or dot notation to access the value of a given property. Here's an example that prints the altText property of the first cat photo - note that the parsed JSON data in the editor is saved in a variable called json:

console.log(json[0].altText);

e.g For the cat with the id of 2, print to the console the second value in the codeNames array. You should use bracket and dot notation on the object (which is saved in the variable json) to access the value: 

document.addEventListener('DOMContentLoaded', function(){

    document.getElementById('getMessage').onclick = function(){

      const req = new XMLHttpRequest();

      req.open("GET",'/json/cats.json', true);

      req.send();

      req.onload=function(){

        const json = JSON.parse(req.responseText);

        document.getElementsByClassName('message')[0].innerHTML = JSON.stringify(json);

        // Add your code below this line

   console.log(json[2].codeNames[1])

        // Add your code above this line

      };

    };

  });

# Conclusion
Tomorrow I will finish the 5 remaining challenges and start with the projects.