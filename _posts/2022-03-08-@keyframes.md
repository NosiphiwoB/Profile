---
Layout:
Title: "javascript"
Date: "2022 03 08"
---

# Introduction
Today I was still busy with the project that was given to us and the @keyframes.


# Body
Today I had to continue with the RSVP form project.I am not done with the project but I did manage to add some few things.Today we were told that if you click "yes" on the "Are You Coming With A Partner?" the partner's food preference should pop up.I was able to do that using :  function showPartner() {
      
      var yesDisplay = document.getElementById("partnerPreference");
      if (yesDisplay.style.display === "none") {
          yesDisplay.style.display = "block";}
     
    }
    function hidePartner() {
        var noDisplay = document.getElementById("partnerPreference");
        if (noDisplay.style.display === "block") {
            noDisplay.style.display = "none";
        }
      }

I also did a revision  on @keyframes,the @keyframes controls what happens during an animation,they contain information of a start (0%) and end (100%) point of an animation.We are able to add many keyframes in one animation.
e.g   @keyframes mymove {
  0%   {top: 0px;}
  25%  {top: 200px;}
  50%  {top: 100px;}
  75%  {top: 200px;}
  100% {top: 0px;}
}

We can also change css styles in one animation
e.g   @keyframes mymove {
  0%   {top: 0px; background: red; width: 100px;}
  100% {top: 200px; background: yellow; width: 300px;}
}

I also learnt that we are able to use CSS @keyframes to change the color of a button in its hover state.For an example if you want to change the width of an image on hover : 
<style>
  img {
    width: 30px;
  }
  img:hover {
    animation-name: width;
    animation-duration: 500ms;
  }

  @keyframes width {
    100% {
      width: 40px;
    }
  }
</style>

<img src="https://cdn.freecodecamp.org/curriculum/applied-visual-design/google-logo.png" alt="Google's Logo" />



# Conclusion
On the rsvp form I am still struggling with aligning the food preference accordingly.