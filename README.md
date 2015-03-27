## Website Performance Optimization portfolio project



############ Reference websites ####
https://piazza.com/
https://developer.chrome.com/devtools/docs/timeline
https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery
https://developers.google.com/speed/articles/optimizing-javascript


############## Tools ###############
https://www.google.com/analytics
https://developers.google.com/speed/pagespeed
http://cssminifier.com/
http://compressnow.com/
http://jscompress.com/

ngrok: https://ngrok.com/
github: https://github.com

###########  Steps I took to optimize the portfolio  ################
I used https://www.google.com/analytics to analyze porfolio web page.
Optimised images by using tinypng.com and compressnow.com

Moved js scripts to the bottom of the html file and made them async

I removed useless style used in css/style.css and inlined css from style.css

I used http://cssminifier.com/ to minify css 

I used http://jscompress.com/ to minify js files.

I added media=print for print.css link inside index.html due that this css file is only used when printing

Removed google font link inside index.html

There were various images that were linked to on the internet. I changed these to local images which have been optimized

main.js

* I used a variable to cache the scrolltop value on line 509 of the main.js file to improve the frames per second

* I added a separate variable on line 455 before for loop, also moved dx and newwidth outside the for loop inside changePizzaSizes function of the main.js file for faster resizing

* Move pizzasDiv variable ouside the loop on line 475 of the main.js file

* I added a separate variable for the faster use of the variable in the updatePosition function on line 509 of the main.js file

* I also use translateX method inside updatePositions function to improve FPS performance

* on line 540, reduced pizza number from 200 to 30, we only need 30 when generates the sliding pizzas on the page

pizza.html

* Took advice from Google Developer Tools Page Speed addon

* Compressed/optimized pizza.png 

* Use inline style-min.css,and minimised bootstrap-grid-min.css 

* Use minimised main.min.js

The improved portfolio can be downloaded from https://github.com/yz2483/frontend-nanodegree-mobile-portfolio.git
To test the page speed I used Python web server and ngrok:

Assume ngrok and Python are downloaded and installed.

1. Via comand Line, go to my porfolio project folder

2. Run command:py -m http.server 7777

3. Open another comand line window

4. Go to ngrok folder

5. Get the public URL of my local web service via command: ngrok 7777 

6. Use the public URL to test page speed on google pagespeend insight - https://developers.google.com/speed/pagespeed/insights

To check the frames per second I used Google Developer Tools
