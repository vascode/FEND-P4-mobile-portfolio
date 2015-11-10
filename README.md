## FEND Project 4 - Website Performance Optimization portfolio project
Demo : http://vascode.github.io/FEND-P4-mobile-portfolio

#### Changes made in view/js/main.js
1.  var pizzasDiv = document.getElementById("randomPizzas") out of the loop
2.  in updatePositions(), pre-calculate following terms
    - var top = document.body.scrollTop/ 1250;
    - var numOfPizzas = items.length;
    then, store repeated five calculated results into array(constArray)
    use translate3d instead of .left to relocate background pizzas' locations
3. scroll event triggers requestAnimationFrame(updatePositions);
4. In handler for DOMContentLoaded, add calculation for how many pizzas need to appear on screen.
5. remove determineDx() as changePizzaSizes() can do a job without it
6. changeSliderLabel() set newWidth as % and changePizzaSizes() set pizza width with it.    

#### Changes made for images (in /img and views/images)
1. img/profilepic.jpg is compressed 
2. views/images/pizzeria.jpg is resized and/or compressed. 
    - index.html links to resized and compressed pic (pizzeria-min.jpg)
    - pizza.html links to compressed pic (pizzeria.jpg)
