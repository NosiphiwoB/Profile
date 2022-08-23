---
Layout:
Title: " Data Visualization"
Date: "2022 08 23"
---

# Introduction
Today I was busy with data visualization,I am trying to finish by the end of this week.

# Body
Tooltip shows more information about an item on a page when the user hovers over that item.We can use the svg 'title' element.'title' pairs with the text() method to dynamically add data to the bars.

e.g 
svg.selectAll("rect")

       .data(dataset)

       .enter()

       .append("rect")

       .attr("x", (d, i) => i * 30)

       .attr("y", (d, i) => h - 3 * d)

       .attr("width", 25)

       .attr("height", (d, i) => d * 3)

       .attr("fill", "navy")

       .attr("class", "bar")

       // Add your code below this line

       .append("title")

       .text((d) => d)

       // Add your code above this line
       
Another type of visualization is scatter plot.It usually uses circles to map data points,which have two values each, these values tie to the x and y axes and are used to position the circle in the visualization.

To create a circle shape  we use circle tag : 

 svg.selectAll("circle")

       // Add your code below this line

       .data(dataset)

       .enter()

       .append("circle")

       // Add your code above this line
       
  The D3 methods domain() and range() set that information for your scale based on the data.There are a couple methods to make that easier.     

Often when you set the domain, you'll want to use the minimum and maximum values within the data set. Trying to find these values manually, especially in a large data set, may cause errors.


D3 has two methods - min() and max() to return this information. Here's an example:

const exampleData = [34, 234, 73, 90, 6, 52];

d3.min(exampleData)

d3.max(exampleData)

A dataset may have nested arrays, like the [x, y] coordinate pairs that were in the scatter plot example. In that case, you need to tell D3 how to calculate the maximum and minimum. Fortunately, both the min() and max() methods take a callback function. In this example, the callback function's argument d is for the current inner array. The callback needs to return the element from the inner array (the x or y value) over which you want to compute the maximum or minimum. Here's an example for how to find the min and max values with an array of arrays:

const locationData = [[1, 7],[6, 3],[8, 3]];

const minX = d3.min(locationData, (d) => d[0]);

minX would have the value 1.

e.g   const positionData = [[1, 7, -4],[6, 3, 8],[2, 9, 3]]

    // Add your code below this line

    const output = d3.max(positionData, (d) => d[2]); // Change this line

    // Add your code above this line

One priority is to set the scale so the visualization fits the SVG container's width and height. You want all the data plotted inside the SVG canvas so it's visible on the web page.

The example below sets the x-axis scale for scatter plot data. The domain() method passes information to the scale about the raw data values for the plot. The range() method gives it information about the actual space on the web page for the visualization.The domain goes from 0 to the maximum in the set. It uses the max() method with a callback function based on the x values in the arrays. The range uses the SVG canvas' width (w), but it includes some padding, too. This puts space between the scatter plot dots and the edge of the SVG canvas:

const dataset = [

  [ 34,    78 ],

  [ 109,   280 ],

  [ 310,   120 ],

  [ 79,    411 ],

  [ 420,   220 ],

  [ 233,   145 ],

  [ 333,   96 ],

  [ 222,   333 ],

  [ 78,    320 ],

  [ 21,    123 ]
];

const w = 500;

const h = 500;

const padding = 30;

const xScale = d3.scaleLinear()

  .domain([0, d3.max(dataset, (d) => d[0])])

  .range([padding, w - padding]);
  
Picture the x-axis as a horizontal line from 0 to 500 (the width value for the SVG canvas).Including the padding in the range() method forces the plot to start at 30 along that line (instead of 0), and end at 470 (instead of 500). 

# Conclusion
For this week I will be busy with D3 because I still need to do the projects (d3) as well.

