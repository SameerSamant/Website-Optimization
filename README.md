Website Performance Optimization portfolio project
===================================================

##Running the project:

Download or clone the repository
To inspect the site on your phone, you can run a local server
Host the website : (below are IIS instruction you can use python or any other  )
1. open IIS manager 
> inetmgr

2. Create a new webiste with a virtual path of the project on port 8080

Download and install ngrok to the top-level of your project directory to make your local server accessible remotely.
>   cd /path/to/your-project-folder
>   ./ngrok http 8080

Copy the public URL ngrok gives you and try running it through PageSpeed Insights! 

Optimizing :
==========
###Part 1: Get better PageSpeed score for index.html
Page score: changes
65: First load;
76: Javascript moved down and made async
86: web font load made async
87: image minified
93: Style.css moved down

###Part 2: Getting Rid of Jank in pizza.html
Average scripting time for 10 frames: Changes
43ms:  first load
32ms: used requestAnimationFrame()
1.5ms: moved document.body.scrollTop  out of for loop

Resize Time: Changes
134ms: First load
4.5ms: removed width calculation to avoid reflow get value from newly created Pizza sizes array


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
