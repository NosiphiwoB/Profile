---
Layout:
Title: " Data Visuliazation"
Date: "2022 08 30"
---

# Introduction
Today managed to finish the five remaining challenges on d3.

# Body
Converting JSON data to HTML --- We can use the forEach method to loop through the data in this case because the cat photo objects are held in an array.As you get to each item, you can modify the HTML elements.
We first declare an html variable with let html = " "; .
Then, loop through the JSON, adding HTML to the variable that wraps the key names in strong tags, followed by the value. When the loop is finished, you render it.

e.g let html = "";

json.forEach(function(val) {

  const keys = Object.keys(val);

  html += "<div class = 'cat'>";

  keys.forEach(function(key) {

    html += "<strong>" + key + "</strong>: " + val[key] + "<br>";

  });

  html += "</div><br>";

});


e.g json.forEach(function(val) {

          // Adding each object keys

          var keys = Object.keys(val);

          // Generating new html

          html += "<div class = 'cat'>";

          // Adding the custom html to each key

          keys.map(function(key) {

            html += "<strong>" + key + "</strong>: " + val[key] + "<br>";

          });

          html += "</div><br>";

        });

Rendering images from data sources --- The last few challenges showed that each object in the JSON array contains an imageLink key with a value that is the URL of a cat's image.
When you're looping through these objects, you can use this imageLink property to display this image in an img element.

Here is how you do this :

html += "<img src = '" + val.imageLink + "' " + "alt='" + val.altText + "'>";


e.g document.addEventListener('DOMContentLoaded', function(){

    document.getElementById('getMessage').onclick = function(){

      const req=new XMLHttpRequest();

      req.open("GET",'/json/cats.json',true);

      req.send();

      req.onload = function(){

        const json = JSON.parse(req.responseText);

        let html = "";

        json.forEach(function(val) {

          html += "<div class = 'cat'>";

          // Add your code below this line

      html += "<img src = '" + val.imageLink + "' " + val.altText + "'>";

          // Add your code above this line

          html += "</div><br>";

        });

        document.getElementsByClassName('message')[0].innerHTML=html;

      };

     };

  });
  
If you don't want to render every photo you get from the freecode camp cat photo API, you can pre-filter the JSON before looping through it.
If the JSON data is stored in an array,you can use the filter method to filter out the cat whose id key has a value of 1.

Here is how you do this :

json = json.filter(function(val) {

  return (val.id !== 1);

});


You can also access your user's current location .Every browser has a built in navigator that can give you this information.The navigator will get the user's current longitude and latitude.You will see a prompt to allow or block this site from knowing your current location. The challenge can be completed either way, as long as the code is correct.By selecting allow, you will see the text on the output phone change to your latitude and longitude.

Here is how you do this: 

if (navigator.geolocation){

  navigator.geolocation.getCurrentPosition(function(position) {

    document.getElementById('data').innerHTML="latitude: " + position.coords.latitude + "<br>longitude: " + position.coords.longitude;

  });

}

First, it checks if the navigator.geolocation object exists. If it does, the getCurrentPosition method on that object is called, which initiates an asynchronous request for the user's position. If the request is successful, the callback function in the method runs. This function accesses the position object's values for latitude and longitude using dot notation and updates the HTML.


You can also send data to an external resource, as long as that resource supports AJAX requests and you know the URL.

JavaScript's XMLHttpRequest method is also used to post data to a server.

e.g const xhr = new XMLHttpRequest();

xhr.open('POST', url, true);

xhr.setRequestHeader('Content-Type', 'application/json; charset=UTF-8');

xhr.onreadystatechange = function () {

  if (xhr.readyState === 4 && xhr.status === 201){

    const serverResponse = JSON.parse(xhr.response);

    document.getElementsByClassName('message')[0].textContent = serverResponse.userName + serverResponse.suffix;

  }

};

const body = JSON.stringify({ userName: userName, suffix: ' loves cats!' });

xhr.send(body);

# Conclusion
Tomorrow I will be writting a test which I am not sure how long it will take but as soon as I finish with the test I will start with the projects.