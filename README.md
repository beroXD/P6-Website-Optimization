## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

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

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
