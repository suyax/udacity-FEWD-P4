Pizza Website Optimization
--------------------------
Course project for Udacity Frontend Nanodegree.
It is a fake pizza website for practice.
By using Chrome Dev. tool and Google Page Speed API to measure page performance.
After measurement, using gulp, grunt and web worker to Optimization CRP by:

HTML:
1. google font will block html dom and css cssom process, font loader was used to improve performance
2. minify and inline key css and javascript to solve block rendering problem
3. js files minify and load at the end will solve js blocking dom and cssom constuction problem
4. async files that not on CRP will improve CRP efficiency
5. cache and server respond time cannot be changed by author

Javascript:
1. solve forced synchronous layouts by reconfigure read and write loop
2. combine size pizza img and switch pizza size and dt functions to make function DRY

Other:
1. use grunt to reduce image size

Instructions
--------------------------
1. Upon loading pizza website has random generated pizzas
2. Upon scroll background changes
3. Drag scale to pick small, middle, large size pizza


Version
--------------------------
v1.0 2015.09.09

Author
--------------------------
Suya Xu

Contact Information
--------------------------
tataxusuya@hotmail.com


