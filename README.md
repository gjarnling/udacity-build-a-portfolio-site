# udacity-build-a-portfolio-site
The fourth project in [Udacity Front-End Developer Nanodegree](https://www.udacity.com/course/front-end-web-developer-nanodegree--nd001) program called "Build a Portfolio Site".

## Description
We were given a design mockup and told to replicate the design using HTML and CSS. The site should be responsive and display images, descriptions and links to each of the projects completed throughout the course of the Nanodegree program.

Apart from the above we were given quite an extensive project rubric including everything from design, responsiveness, seperation of concerns to code quality.

## Prerequisites
This block of lessons is the longest in the whole of the course clocking in at 33.5 hours. It is made up of five blocks:

* Sizing Elements
* Intro to HTML and CSS
* Responsive Web Design Fundamentals
* Responsive Images
* Project

Below are a short summary of each block; this is in no way a comprehensive or detailed explanation of the content covered.

### Sizing Elements
The first block covered [the CSS box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model) and [semantic elements in HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5). After this we were given a related problem set.

### Intro to HTML and CSS
The second block started with repetition of HTML, CSS, and Boxes. It then went on to handle responsive layout and CSS Frameworks. To start of we created out own framework for responsive layouts.

We then looked at other frameworks, including [Bootstrap](http://getbootstrap.com/). During this block we were given quizes to make us more familiar with what Bootstrap has to offer. We also looked at how to customize Bootstrap to include the features you need and why minified versions are prefered.

### Responsive Web Design Fundamentals
This block started off with a discussion about why responsiveness matters. We looked at sites on mobile and set up our workflow, using [Chrome's Dev Tools](https://developer.chrome.com/devtools) for device emulation as well as remote debugging on mobile devices.

We then looked at why starting small and building up is the way to go. It covered things like pixelation, DPR, CSS pixels, viewports and relative sizes. Apart from that it contained a discussion on tap targets and tap target sizes.

Lesson three covered the use of media queries, how to pick breakpoints and why the content should be the guide of doing so. It also covered grids and how to set them up using [CSS Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes).

The fourth lesson in this block covered common responsive layouts. In summary I really enjoyed this part and having this knowledge makes the transition from design to code a lot easier. The patterns covered were column drop, mostly fluid, layout shifter, and off canvas.

The fifth and last lesson in this block covered responsive tables and once again introduced three design patterns for dealing with them: hidden columns, no more tables, and contained scrolling. It also covered how to make fonts responsive and defining minor breakpoints.

### Repsonsive Images
The first lesson was basically a short repition covering the importance of responsive images and how to setup remote debugging on mobile.

The second lesson covered different ways to size images. It also introduced some less known CSS units. Apart from this it treated different types of images and when to use which. Lastely it looked out how to optimize images and the related workflow using [Grunt](http://gruntjs.com/).

The third lesson covered using markup as images. Everything from CSS background images, [Unicode symbol characters](http://unicode-table.com/en/#control-character) to [icon fonts](http://weloveiconfonts.com/).

The fourth and last lesson covered how to make images fully responsive using [the image elements srcset and sizes attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img), the [picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) and [source](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source) elements. It also covered accessibility concerning images.

## Solution
Most concepts presented in the course I knew since before. But some of them were new to me, so I decided to stick with those when implementing the project to get experience using them.

As for design I decided to stick with the design mockup we had been given. We were told to experiment and of course personalize it, which I did. But the overall layout, which we can call "traditional", was kept.

For implementing the layout we had the option to either use a framework or to build our layout using flexbox. I have worked with flexbox before but never enough to make me really comfortable, so I chose to use it. A reference I came back to again and again during development was [CSS Tricks A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/). I highly recommend it.

Much of the course covered responsive images. Since [images makes up for the most bytes per page by content type on avarage](http://mobile.httparchive.org/interesting.php#bytesperpage) this makes a lot of sense. The use of [srcset and sizes attributes on images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images#How_do_you_create_responsive_images) aswell as the [picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture) and [source](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source) elements were new to me, so I wanted to use these as much as possible. I went through several iterations of the site before I finished it and put most of the effort into using these techniques. I'm also glad I spent a lot of time getting to know and using [Grunt](http://gruntjs.com/) with [grunt-responsive-images](http://www.andismith.com/grunt-responsive-images/) and [GraphicsMagick](http://www.graphicsmagick.org/). Weather I will use Grunt or some other task manager I'm very happy to feel comfortable with the workflow, since it speed things up a lot when working with a big amount of images.

For remote debugging I ended up using a tool not mentioned in the course material called [Ghostlab](https://www.vanamco.com/ghostlab/). So far I have been very pleased with this choice.

## Closure
The solution met the specifications.
