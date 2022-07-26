---
Layout:
Title: " Data Visualization"
Date: "2022 07 25"
---

# Introduction
Today I started with  Data Visualization.D3, or D3.js, stands for Data Driven Documents. It's a JavaScript library for creating dynamic and interactive data visualizations in the browser.

# Body 
D3 is built to work with common web standards – namely HTML, CSS, and Scalable Vector Graphics (SVG).D3 (Data Driven Documents) is a javascript library for creating dynamic and  interactive data visualization in the browser.

*select() ---selects one element from the document. It takes an argument for the name of the element you want and returns an HTML node for the first element in the document that matches the name.

*append() ---takes an argument for the element you want to add to the document. It appends an HTML node to a selected item, and returns a handle to that node.

*text() ----either sets the text of the selected node, or gets the current text. To set the value, you pass a string as an argument inside the parentheses of the method.

D3 allows us to chain several methods together.

e.g <body>


  <script>


    // Add your code below this line


d3.select("body")


  .append("h1")


  .text("Learning D3")


    // Add your code above this line


  </script>


</body>


We also have the selectAll() method which select a group of elements
e.g const anchors = d3.selectAll("a");

e.g Select all of the li tags in the document, and change their text to the string list item by chaining the .text() method: 


<body>


  <ul>


    <li>Example</li>


    <li>Example</li>


    <li>Example</li>


  </ul>


  <script>


    // Add your code below this line


d3.selectAll("li")


  .text("list item")


    // Add your code above this line


  </script>


</body>


This will return a new list 


-list item


-list item


-list item


data() is used on a selection of DOM elements to attach the data to those elements.The data set is passed as an argument to the method
enter() is ussed to create a new element in the document for each piece of data in the set .


e.g <body>


  <script>


    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];


    // Add your code below this line


d3.select("body").selectAll("h2")


  .data(dataset)


  .enter()


  .append("h2")


  .text("New Title")


    // Add your code above this line


  </script>


</body>


This code is telling D3 to first select the body on the page. Next, select all h2 elements, which returns an empty selection. Then the data() method reviews the dataset and runs the following code nine times, once for each item in the array. The enter() method sees there are no h2 elements on the page, but it needs 9 (one for each piece of data in dataset). New h2 elements are appended to the body and have the text New Title.


The D3 text() method can take a string or a callback function as an argument:


selection.text((d) => d)


In the example above, the parameter d refers to a single entry in the dataset that a selection is bound to.

e.g Change the text() method so that each h2 element displays the corresponding value from the dataset array with a single space and the string USD. For example, the first heading should be 12 USD:


<body>


  <script>


    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];


    d3.select("body").selectAll("h2")


      .data(dataset)


      .enter()


      .append("h2")

      
      // Add your code below this line


   .text((d) => d +' USD');


      // Add your code above this line


  </script>
  

</body>


style() adds inline css style on a dynamic element.The style() method takes a comma-separated key-value pair as an argument

e.g selection.style("color","blue");

# Conclusion
I am going to continue with data visualization.