---
Layout:
Title: " Data Visualization"
Date: "2022 07 26"
---

# Introduction
I am still busy with  data visualization.

# Body
You can use a callback function in the style() method to change the styling for different elements.


e.g <body>


  <script>

    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];


    d3.select("body").selectAll("h2")


      .data(dataset)


      .enter()


      .append("h2")


      .text((d) => (d + " USD"))


      // Add your code below this line


     .style("color", (d) => {


       if(d < 20){


         return "red"


       } else {


         return "green"


       }


     })


   // Add your code above this line


  </script>


</body>


D3 has the attr() method to add any HTML attribute to an element, including a class name.The attr() method works the same way that style() does. It takes comma-separated values, and can use a callback function.


e.g <style>


  .bar {


    width: 25px;


    height: 100px;


    display: inline-block;


    background-color: blue;


  }


</style>


<body>


  <script>


    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];


    d3.select("body").selectAll("div")


      .data(dataset)


      .enter()


      .append("div")


      // Add your code below this line


     .attr("class", "bar")


      // Add your code above this line


  </script>


</body>


To create a simple bar chart to create a div for each data point in the array and we need to also give each dynamic height,using  a callback function in the style() method that sets height equal to the data value.


e.g <style>


  .bar {


    width: 25px;


    height: 100px;


    display: inline-block;


    background-color: blue;


  }


</style>


<body>


  <script>


    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];


    d3.select("body").selectAll("div")


      .data(dataset)


      .enter()


      .append("div")


      .attr("class", "bar")


      // Add your code below this line


     .style("height", (d) => d + "px")


      // Add your code above this line


  </script>


</body>


To add spaces between each bar we add a margin to the css for the bar class.
To increase the height for the bars to show the differece in values ,we multiply the value by a number to scalethe height.


e.g <style>


  .bar {


    width: 25px;


    height: 100px;


    /* Add your code below this line */


    margin: 2px;

    
    /* Add your code above this line */


    display: inline-block;


    background-color: blue;


  }


</style>


<body>


  <script>



    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];


    d3.select("body").selectAll("div")


      .data(dataset)


      .enter()


      .append("div")


      .attr("class", "bar")


      .style("height", (d) => (d * 10)) // Change this line


  </script>


</body>


SVG --stands for Scalable Vector Graphics.Here "scalable" means that, if you zoom in or out on an object, it would not appear pixelated. It scales with the display system, whether it's on a small mobile screen or a large TV monitor.When you place a shape into the svg area, you can specify where it goes with x and y coordinates


e.g const svg = d3.select("body")


                  .append("svg")


                  .attr("width", w)


                  .attr("height", h)


                  // Add your code below this line


                  .append("rect")


                  .attr("width","25")


                  .attr("height","100")


                  .attr("x","0")


                  .attr("y","0")
                  

For a bar chart, all of the bars should sit on the same vertical level, which means the y value stays the same (at 0) for all bars. The x value, however, needs to change as you add new bars. Remember that larger x values push items farther to the right. As you go through the array elements in dataset, the x value should increase.The attr() method in D3 accepts a callback to dynamically set that attribute.
Here is a format :


selection.attr("x", (d, i) => {


        return i * 30


       })


To set the bars right-side-up :


selection.attr("y", (d, i) => {


return h -3 * d


}


In SVG, a rect shape is colored with the fill attribute :


selection.attr("fill","navy")


Adding labels to D3 elements:


selectAll("text")


       .data(dataset)


       .enter()


       // Add your code below this line


       .append("text")


       .attr("x", (d, i) => i * 30)


       .attr("y", (d, i) => h - 3 * d - 3)


       .text((d, i) => d);


# Conclusion
For now I am going to continue with data visualization and also try to do some project for better understanding.