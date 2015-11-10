## Website Performance Optimization portfolio project
Demo : 

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
6. In changePizzaSizes(), set newWidth as % and set pizza size with it. 
