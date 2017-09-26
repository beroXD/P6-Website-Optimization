## Website Performance Optimization portfolio project

This is my 6th project in the Udacity Front-End Web Developer Nanodegree Program.

The goal of this project is:
- Optimize `index.html` to score a speed above 90 for mobile and Desktop.
- Optimize `views/js/main.js` to make `views/pizza.html` render with a consistent frame-rate at 60fps when scrolling.

### Getting started

- Download the repository.
- `src` file contain the source code.
- `dist` file contain the production code.
- Open `index.html`

#### Part 1: Optimize PageSpeed Insights score for index.html

1. Compressed and resized images using Photoshop and [compressimage.toolur](http://compressimage.toolur.com/)
2. Removed extra css that is not used.
3. Used media query to prevent print.css from render blocking.
4. Inlined style.css in html and minified html.
5. Removes google analytics link, could not see if it was doing any work.
5. Improved score to 96 for Desktop and 94 for mobile.

#### Part 2: Optimize Frames per Second in pizza.html

1. Compressed and resized pizzeria image.
2. Added ```will-change: transform;``` and ```transform: translateZ(0);``` to style.css
3. Replaced ```querySelectorAll```, ```querySelector``` with ```getElementById```, ```getElementsByClassName```
4. Removed determineDx function, it does unnecessary work.
5. When resizing pizza there is no need for px width, % width is enough.
7. Added ```requestAnimationFrame```
8. Optimized loops in ```updatePositions```
9. Getting the width and height of screen then creating pizzas based on the rows and cols of the screen.
