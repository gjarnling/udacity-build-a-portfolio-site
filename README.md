# udacity-build-a-portfolio-site
The fourth project in [Udacity Front-End Developer Nanodegree](https://www.udacity.com/course/front-end-web-developer-nanodegree--nd001) program called "Build a Portfolio Site".

## Description
Replicate a design mockup using HTML and CSS. The site should be responsive and display images, descriptions and links to each of the projects completed throughout the course of the Nanodegree program.

The above guidelines came with quite an extensive project rubric including everything from design, responsiveness, seperation of concerns to code quality.

## Prerequisites
This course is the longest of the program clocking in at 33.5 hours. It is made up of five blocks:

* Sizing Elements
* Intro to HTML and CSS
* Responsive Web Design Fundamentals
* Responsive Images
* Project

Below is a short summary of each block; just be adviced that this in no way is a comprehensive or detailed explanation of the content covered.

### Sizing Elements
The first block covered [the CSS box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model) and [semantic elements in HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5). It was followed by a related problem set.

### Intro to HTML and CSS
The second block started with a repetition of HTML, CSS, and Boxes. Responsive layout and CSS Frameworks were introduced and a framework for responsive layouts were created.

It then dealt with other frameworks, including [Bootstrap](http://getbootstrap.com/). To segment the knowledge of Bootstrap many quizzes were given. Finally went through how to customize Bootstrap to include only selected features and why minified versions are prefered.

### Responsive Web Design Fundamentals
The third block started off with a discussion about why responsiveness matters and several web sites were showed on mobile. Then showed how to set up the workflow using [Chrome's Dev Tools](https://developer.chrome.com/devtools) for device emulation as well as remote debugging on mobile devices.

It then explained why starting small and building up is the way to go, covering things like pixelation, DPR, CSS pixels, viewports and relative sizes. Targets and tap target sizes were also discussed.

Lesson three covered the use of media queries, how to pick breakpoints and why the content should be the guide of doing so. It also covered grids and how to set them up using [CSS Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes).

The fourth lesson in this block covered common responsive layouts and how these make the transition from design to code a lot easier. The patterns covered were column drop, mostly fluid, layout shifter, and off canvas.

The fifth and last lesson in this block covered responsive tables and once again introduced three design patterns for dealing with them: hidden columns, no more tables, and contained scrolling. It also covered how to make fonts responsive and defining minor breakpoints.

### Repsonsive Images
The first lesson was basically a short repetition covering the importance of responsive images and how to setup remote debugging on mobile.

The second lesson covered different ways to size images with CSS. It also introduced some lesser known CSS units. Apart from this it treated different types of images, like JPEG, PNG and SVG, and when to use which and why. Lastely it looked out how to optimize images and the related workflow using [Grunt](http://gruntjs.com/).

The third lesson covered using markup as images. Everything from CSS background images, [Unicode symbol characters](http://unicode-table.com/en/#control-character) to [icon fonts](http://weloveiconfonts.com/).

The fourth and last lesson covered how to make fully responsive images using [the image element srcset and sizes attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img), the [picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) and [source](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source) elements. It also covered accessibility in regard to images.

## Solution
Most concepts presented in the course I knew since before. But some of them were new to me, so I decided to stick with those when implementing the project to get experience using them.

Regarding the layout we had the option to either use a framework like Bootstrap or to build our layout using CSS flexbox. I have worked with flexbox before but never enough to make me really comfortable, so I chose to use it. A reference I came back to again and again during development was [CSS Tricks "A Complete Guide to Flexbox"](https://css-tricks.com/snippets/css/a-guide-to-flexbox/). I highly recommend it.

Much of the course covered responsive images. Since [images makes up for the most bytes per page by content type on avarage](http://mobile.httparchive.org/interesting.php#bytesperpage) this makes a lot of sense. The use of [srcset and sizes attributes on images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images#How_do_you_create_responsive_images) aswell as the [picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) and [source](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source) elements were new to me, so I wanted to use these as much as possible. I went through several iterations of the site before I finished it and put most of the effort into using these techniques. To make sure the picture and source elements will be rendered on all browsers I also used a JavaScript polyfill named [Picturefill](http://scottjehl.github.io/picturefill/).

I'm also glad I spent a lot of time getting to know and using [Grunt](http://gruntjs.com/) with [grunt-responsive-images](http://www.andismith.com/grunt-responsive-images/) and [GraphicsMagick](http://www.graphicsmagick.org/). Weather I will use Grunt or some other task manager I'm very happy to feel comfortable with the workflow, since it speed things up a lot when working with a big amount of images.

For remote debugging I ended up using a tool not mentioned in the course material called [Ghostlab](https://www.vanamco.com/ghostlab/). So far I have been very pleased with this choice.

### Design & Implementation
We were given a design mockup but told to personalize it, since after all it's our own portfolio. I chose to stick with the basic layout given therein. The site contains three parts:

* Header
* Main content
* Footer

Even tho this isn't a design course I made some overall decisions regarding the design. I chose to use the [Futura PT font from Paratype](http://www.paratype.com/pstore/fonts/Futura-PT.htm) served by [Adobe TypeKit](https://typekit.com/) as my font for the whole site. For colors I went with a dark grey and several different opacities, inspired by the [Google Material Design guidelines](https://material.google.com/).

I also chose to use the [Google Material Design Web Icon Font](https://design.google.com/icons/) for smaller icons. The main source of colors come from the header image, an abstract painting. To add some more contrast I also added a background to the site, mainly visible in the lower part. The header image is the only rasterized image (JPEG) used on the site, the rest are vectorised SVG files to keep the file sizes as small as possible without losing the ability to scale.

Working from small to big, in the small layout everything is stacked on top of each other. Using the content as guidance I found out I needed three major breakpoints:

* 600 pixels: Change header and present main content in two columns
* 870 pixels: Present main content in three columns
* 1100 pixels: Set max width to content and center it

Of course all files used are valid [HTML5](https://www.w3.org/TR/html5/) and [CSS3](https://www.w3.org/Style/CSS/) files, validated with [W3C HTML Validator](https://validator.w3.org/) and [W3C CSS Validator](https://jigsaw.w3.org/css-validator/).

#### Header
The header contains a logo, my name and title. It also contains a image of an abstract painting.

Their representation changes depending on the viewport size. For smaller viewports they are presented on top of each other; the logo, my name, my title and the painting one after the other. On larger viewports the logo moves to the left with my name and title to the right and the image now set as a background.

In its original state the image is huge at 10.2MB with the dimensions 3390x3671 pixels. First I cropped it to only contain the part I wanted. This reduced the size to 2.23MB and the dimensions to 3390x1323 pixels. Since the content of the site never will grow larget than 1100 pixels I decided to set a maximum size of the image to 2200 pixel, to accomodate screens with a higher pixel density.

With my major breakpoints as a guideline I used Grunt to create five images for different viewport sizes. I also decided that a compression level of 50 kept the quality of the photo. This way the file size was dramatically reduced to 439kB for the biggest all the way down to 48.1kB for the smallest.

Using the picture and source elements the browser only fetch a big enough image for the viewport, taking the screen pixel density into account.

#### Main Content
The main content contains one header: Featured work. After that each projected is listed and represented as a card. Notice that even tho the projects are listed in the correct order in the source HTML file they represented in the reverse order on the site.

Every card has a header image on top followed by a card header. After that is a short description of the project. On the bottom each card has three links; one leading to more information about the project, one to the source file(s), and one to view the final result.

On small viewports each card is stacked one on top of the other. The first major breakpoint puts the main content into two columns. This is turned into three columns by the third major breakpoint.

#### Footer
The footer contains two blocks of content. One part contains social media icons for sharing the site. The other part contains a very short colophon.

On smaller viewports the social media links are presented on top of the colophon. The second major breakpoint puts the colophon to the left while the social media links are put to the right. This stays the same during the third breakpoint.

## Closure
The solution met the specifications.
