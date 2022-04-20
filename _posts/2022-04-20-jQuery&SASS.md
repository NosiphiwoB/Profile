---
Layout:
Title: "jQuery and SASS"
Date: "2022 04 20"
---

# Introduction
Today I managed to finish the challenges that were remaining in jQuery and I also started with SASS.

# Body
As we can add classes to an element with jQuerys addClass() function we can also remove them with jQuerys removeClass() function
e.g $("#target2").removeClass("btn-default");

We can also change the CSS of an HTML element directly with jQuery.
e.g $("#target1").css("color", "blue"); . 
This is slightly different from a normal CSS declaration, because the CSS property and its value are in quotes, and separated with a comma instead of a colon.We also able to disable an element using jQuery, we have a function called .prop() that allows us to adjust the properties of elements.
e.g $("button").prop("disabled", true); .


We can change the text between the start and end tags of an element, jQuery has a function called .html() that allows us to add html tags and text within an element.Any content previously within the element will be completely replaced with the content you provide using this function.
e.g `$("h3").html("<em>jQuery Playground</em>");` .
jQuery also has a similar function called .text() that only alters text without adding tags. In other words, this function will not evaluate any HTML tags passed to it, but will instead treat it as the text you want to replace the existing content with.

As we are able to remove classes we are also able to remove elements using jQuery, we use function called .remove() which removes an html element entirely
e.g $("#target4").remove()


jQuery has a function called appendTo() that allows us to select html elements and append them to another element.
For example, if we wanted to move target4 from our right well to our left well, we would use:

$("#target4").appendTo("#left-well"); .

We also have function called clone() that makes a copy of an element
For example, if we wanted to copy target2 from our left-well to our right-well, we would use:

$("#target2").clone().appendTo("#right-well"); . 

So here we have to chain two functions which is a convenient way to get things done with jQuery.


We also have a function called parent() which allows us to access the parent of whichever element we have selected.Here's an example of how you would use the parent() function if you wanted to give the parent element of the left-well element a background color of blue:

$("#left-well").parent().css("background-color", "blue")

As we are able to access the parents we are also able to access the children of whichever element we have selected using the fuction called children()

eg $("#left-well").children().css("color", "blue")



We have the target:nth-child(n) css selector that allows us to select all the nth elements with the target class or element type
Here's how you would give the third element in each well the bounce class:

$(".target:nth-child(3)").addClass("animated bounce");


We can also target elements based on their positions using :odd or :even selector, jQuery is also zero-indexed meaning the first element in a selection has a position of 0.Here's how you would target all the odd elements with class target and give them classes:

$(".target:odd").addClass("animated shake");

jQuery can target the body element as well.Here's how we would make the entire body fade out: $("body").addClass("animated fadeOut");


SASS 
Sass, or "Syntactically Awesome StyleSheets", is a language extension of CSS. It adds features that aren't available in basic CSS, which make it easier for you to simplify and maintain the style sheets for your projects.

In SASS variables start with a $ followed by a variable name.
e.g $main-fonts: Arial, sans-serif;
$headings-color: green;

And to use the variables:
h1 {
  font-family: $main-fonts;
  color: $headings-color;
} .
One example where variables are useful is when a number of elements need to be the same color. If that color is changed, the only place to edit the code is the variable value.

Here is another example
Create a variable $text-color and set it to red. Then change the value of the color property for the .blog-post and h2 to the $text-color variable:

<style type='text/scss'>
  $text-color:red;

  .blog-post, h2 {
    color: red;
    color:$text-color;
  }
</style> .


Normally each element is targeted on a different line to style it :

nav {

  background-color: red;
  
}

nav ul {

  list-style: none;
  
}

nav ul li {

  display: inline-block;
  
}

Nesting can help to orginize the code by placing child style rules within the respective parent element :

nav {

  background-color: red;

  ul {
  
    list-style: none;

    li {
    
      display: inline-block;
      
    }
  }
} .

# Conclusion
Tomorrow I will be doing the remaining challenges on SASS and move on to the next course.