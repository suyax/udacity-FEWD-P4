Portfolio page & Pizza Website Optimization
--------------------------

Introduction
--------------------------

Course project for Udacity Front-end Nanodegree.
There is a fake portfolio page and a fake pizza website for practice.
By using Chrome Dev. tool and Google Page Speed API to measure page performance.
After measurement, optimize CSS,JS and HTML and also using grunt for minify files and images:


Portfolio Page
--------------------------


Optimizations:

1. Google font will block html dom and css cssom process, font loader was used to improve performance
2. Minify and in-line key CSS to solve block rendering problem
3. Async scripts that not on CRP will improve CRP efficiency
4. Move non-CRP scripts to the end of body tag
5. Optimize images using grunt (please see detail at Pizza Website Optimization)


Pizza Website Optimization
--------------------------

	A. HTML:

		1. Minify and In-line key css to solve block rendering problem (please see minify css detail at Grunt)
		2. Responsive Images: by switching imgs according to windows width (please see responsive and minify images detail at Grunt)
		3. Minify JS script and move it to the end of body tag

	B. Java script:

		1. Add use strict (line 1)
		2. In makeRandomPizza function: and sauce and crust in one step(line 446)
		3. Combine size pizza images and switch pizza size text and dt functions into resizePizzas functions to make function DRY (line 493)
		4. Use document.getElementsByClassName() instead of querySelectorAll() for better performance for all instances(line 517,572)
		5. Use document.getElementById() instead of query selector()(line 503,507,511,538,606)
		5. When define for loop: replace hard entered number to variable name to reduce hard code(line 519,540,598)
		6. Optimize functions by move variable definition out of for loop(line 597) and do the calculation for a fixed number before pass into the loop; (line 573)
		7. replace style.left by style.transform.translateX() for better performance(line 575) and change the location item according to current position
		8. At the event DOMContentLoaded, generates number of pizzas based on window.innerHeight to help with performance.(line 596)

	C. CSS:

		1.Hardware-accelerate graphics-intensive CSS features by offloading them to the GPU for better rendering performance on .mover(line 30)
		2. Width of col set to inhert to fix pizza icon start with different size


	D. Grunt-work-flow:

		Initiate npm and Grunt to prepare gruntfile.js and package.json in project folder install different node_modules. Load and register grunt modules in gruntfile.js and run grunt in terminal for work flow management:

		1. Run jshint & watch for monitoring code quality in terminal.
		2. Run uglify & cssmin for minifying JS and CSS file and saved them in dest folder
		3. Run responsive_images and imagemin to resize and optimizes images (Mozilla JPEG Encoder)and saved them in dest/image folder

Instructions
--------------------------

1. Upon loading, pizza website has random generated pizzas with different toppings
2. Upon scroll background changes
3. Drag scale to pick small, middle, large size pizza and text label and all pizza icon on the page will change accordingly.


Version
--------------------------
v3.0 2015.09.20
Notes: 1.pizza menu icon start at same size
	   2.bug with start background only have one col of pizza fixed
	   3.bug with background pizza shift only happen to half of the screen fixed

Author
--------------------------
Suya Xu

Contact Information
--------------------------
tataxusuya@hotmail.com
