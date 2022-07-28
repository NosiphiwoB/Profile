---
Layout:
Title: " Data Visualization"
Date: "2022 07 27"
---

# Introduction
Today I was busy with data visualization.

# Body
We can also add the effect that highlight a bar when the user hovers over it with the mouse.We can do that using css.You set the CSS class on the SVG elements with the attr() method. Then the :hover pseudo-class for your new class holds the style rules for any hover effects.


e.g <style>

  .bar:hover {

    fill: brown;

  }

</style>

 svg.selectAll("rect")

    .attr("class", "bar")
    

A tooltip shows more information about an item on a page when the user hovers over that item. 

e.g selection.append("title")

      .text((d) => d)
      
Here we used the title element,we paired it with the text() method to dynamically add data to the bars.      

A scatter plot is another type of visualization. It usually uses circles to map data points, which have two values each.These values tie to the x and y axes, and are used to position the circle in the visualization.We use the circle tag to create the circle shape

e,g svg.selectionAll("circle")

       .data(dataset)

       .enter()

       .append("circle")
       
The circle in svg has 3 attribute. The cx and cy attributes are the coordinates.  The radius (r attribute) gives the size of the circle.

e.g svg.selectAll("circle")

       .data(dataset)

       .enter()

       .append("circle")

       // Add your code below this line

       .attr("cx",(d)=>d[0])

       .attr("cy",(d)=>h-d[1])

       .attr("r", "5")

The text nodes need x and y attributes to position it on the SVG canvas. In this challenge, the y value (which determines height) can use the same value that the circle uses for its cy attribute. The x value can be slightly larger than the cx value of the circle, so the label is visible. This will push the label to the right of the plotted point.

e.g Label each point on the scatter plot using the text elements. The text of the label should be the two values separated by a comma and a space. For example, the label for the first point is 34, 78. Set the x attribute so it's 5 units more than the value you used for the cx attribute on the circle. Set the y attribute the same way that's used for the cy value on the circle:

 svg.selectAll("text")

       .data(dataset)

       .enter()

       .append("text")

       // Add your code below this line

      .text((d) => (d[0] + ", " + d[1]))

       .attr("x" , (d) => d[0] +5)

       .attr("y", (d) => h-d[1])

# Conclusion
I am going to continue with data visualization.
