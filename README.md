## Website Performance Optimization portfolio project

## How To use
To use this portfolio open index.html in a web browser.
Clicking on the "Cam's Pizzeria" link will take you to the pizzeria page that underwent revision to run at 60 fps!

## Optimizations
The following optimizations were performed on the main page :
1. The css was minified and inlined (http://cssminifier.com/)
2. Since neither external js file was necessary for page rendering they were both set to async
3. The Google webfont was linked via some javascript trickery found in their CSS Delivery recommendations (https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery#example)
4. The pizzeria image and profile image were resized/resampled to reduce their size.
5. Print rules stylesheet had the "print" media type applied to dictate to only load it on print.
6. Javascript minified (http://javascript-minifier.com/)

The following optimizations were performed on the pizzeria webpage via views/js/main.js :
1. In the resizePizzas function I created a pizzaContainers variable that would hold the results of looking up all of the pizza containers on the page. This was an improvement over calling the 
entire collection of pizza containers on each loop iteration! I also pulled the width calculations out of the loop, since it only needed to be calculated once and then applied to the pizzas in the loop.
2. In the updatePositions function I pulled the calculation of the current position from top out of the loop. Again this only needed to be calculated once and then applied inside the loop.

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

