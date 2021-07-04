# Readings : Audio, Video, Images

# Images #

* Controling img size

> You can control the size of an
image using the width and
height properties in CSS, just
like you can for any other box.
Specifying image sizes helps
pages to load more smoothly
because the HTML and CSS
code will often load before the
images, and telling the browser
how much space to leave for an
image allows it to render the rest
of the page without waiting for
the image to download.
You might think that your site
is likely to have images of all
different sizes, but a lot of sites
use the same sized image across
many of their pages.
For example, an e-commerce site
tends to show product photos
at the same size. Or, if your site
is designed on a grid, then you
might have a selection of image
sizes that are commonly used on
all pages, such as:
Small portrait: 220 x 360
Small landscape: 330 x 210
Feature photo: 620 x 400
Whenever you use consistently
sized images across a site,
you can use CSS to control
the dimensions of the
images, instead of putting the
dimensions in the HTML.

```html 
<img src="images/magnolia-large.jpg"
class="large" alt="Magnolia" />
<img src="images/magnolia-medium.jpg"
class="medium" alt="Magnolia" />
<img src="images/magnolia-small.jpg"
class="small" alt="Magnolia" />
```

```css
img.large {
width: 500px;
height: 500px;}
img.medium {
width: 250px;
height: 250px;}
img.small {
width: 100px;
height: 100px;}
```

* Aliging img

> In the last chapter, you saw how
the float property can be used
to move an element to the left or
the right of its containing block,
allowing text to flow around it.
Rather than using the <img>
element's align attribute, web
page authors are increasingly
using the float property to align
images. There are two ways that
this is commonly achieved:
1: The float property is added
to the class that was created to
represent the size of the image
(such as the small class in our
example).
2: New classes are created with
names such as align-left or
align-right to align the images
to the left or right of the page.
These class names are used in
addition to classes that indicate
the size of the image.
In this example you can see the
align-left and align-right
classes used to align the image.
It is also common to add a
margin to the image to ensure
that the text does not touch their
edges.

```html 
<p><img src="images/magnolia-medium.jpg"
alt="Magnolia" class="align-left medium" />
<b><i>Magnolia</i></b> is a large genus that
contains over 200 flowering plant species...</p>
<p><img src="images/magnolia-medium.jpg"
alt="Magnolia" class="align-right medium" />
Some magnolias, such as <i>Magnolia stellata</i>
and <i>Magnolia soulangeana</i>, flower quite
early in the spring before the leaves open...</p>
```

```css
img.align-left {
float: left;
margin-right: 10px;}
img.align-right {
float: right;
margin-left: 10px;}
img.medium {
width: 250px;
height: 250px;}
```

* Centering img

> By default, images are inline
elements. This means that they
flow within the surrounding text.
In order to center an image, it
should be turned into a blocklevel
element using the display
property with a value of block.
Once it has been made into a
block-level element, there are
two common ways in which you
can horizontally center an image:
1: On the containing element,
you can use the text-align
property with a value of center.
2: On the image itself, you can
use the use the margin property
and set the values of the left and
right margins to auto.
You can specify class names
that allow any element to be
centered, in the same way that
you can for the dimensions or
alignment of images.
The techniques for specifying
image size and alignment of
images can also be used with
the HTML5 < figure> element,
which you met on page 119.

```html
<p><img src="images/magnolia-medium.jpg"
alt="Magnolia" class="align-center medium" />
<b><i>Magnolia</i></b> is a large genus that
contains over 200 flowering plant species. It
is named after French botanist Pierre Magnol and,
having evolved before bees appeared, the
flowers were developed to encourage pollination
by beetle.</p>
```

```css
img.align-center {
display: block;
margin: 0px auto;}
img.medium {
width: 250px;
height: 250px;}
```

* Background Images

> The background-image
property allows you to place
an image behind any HTML
element. This could be the entire
page or just part of the page. By
default, a background image will
repeat to fill the entire box.
The path to the image follows
the letters url, and it is put
inside parentheses and quotes.
Here is the image
tile used in this
example.
In the first example, you can
see a background image being
applied to an entire page
(because the CSS selector
applies to the <body> element).
In the second example, the
background image just applies to
a paragraph.
If you search online, you will
find lots of resources that offer
background textures that you
can use on your pages.
Background images are often
the last thing on the page to
load (which can make a website
seem slow to load). As with any
images you use online, if the
size of the file is large it will take
longer to download.

```css
body {
background-image: url("images/pattern.gif");} 
```

* Repeating Images 

> The background-repeat
property can have four values:
repeat
The background image is
repeated both horizontally and
vertically (the default way it
is shown if the backgroundrepeat
property isn't used).
repeat-x
The image is repeated
horizontally only (as shown in
the first example on the left).
repeat-y
The image is repeated vertically
only.
no-repeat
The image is only shown once.
The background-attachment
property specifies whether a
background image should stay in
one position or move as the user
scrolls up and down the page. It
can have one of two values:
fixed
The background image stays in
the same position on the page.
scroll
The background image moves
up and down as the user scrolls
up and down the page.

```css
body {
background-image: url("images/header.gif");
background-repeat: repeat-x;}
```

* Background Position

```css
body {
background-image: url("images/tulip.gif");
background-repeat: no-repeat;
background-position: center top;}
```

* shorthand 

```css
body {
background: #ffffff url("images/tulip.gif")
no-repeat top right;}
```

* Image Rollovers 

```css
a.button {
height: 36px;
background-image: url("images/button-sprite.jpg");
text-indent: -9999px;
display: inline-block;}
a#add-to-basket {
width: 174px;
background-position: 0px 0px;}
a#framing-options {
width: 210px;
background-position: -175px 0px;}
a#add-to-basket:hover {
background-position: 0px -40px;}
a#framing-options:hover {
background-position: -175px -40px;}
a#add-to-basket:active {
background-position: 0px -80px;}
a#framing-options:active {
background-position: -175px -80px;}
```

* Gradients

```css
#gradient {
/* fallback color */
background-color: #66cccc;
/* fallback image */
background-image: url(images/fallback-image.png);
/* Firefox 3.6+ */
background-image: -moz-linear-gradient(#336666,
#66cccc);
/* Safari 4+, Chrome 1+ */
background-image: -webkit-gradient(linear, 0% 0%,
0% 100%, from(#66cccc), to(#336666));
/* Safari 5.1+, Chrome 10+ */
background-image: -webkit-linear-gradient(#336666,
#66cccc);
/* Opera 11.10+ */
background-image: -o-linear-gradient(#336666,
#66cccc);
height: 150px;
width: 300px;}
```

* Exam 

```css
<!DOCTYPE html>
<html>
<head>
<title>Images</title>
<style type="text/css">
body {
color: #665544;
background-color: #d4d0c6;
background-image: url("images/backdrop.gif");
font-family: Georgia, "Times New Roman", serif;
text-align: center;}
.wrapper {
width: 720px;
margin: 0px auto;}
.header {
margin: 40px 0px 20px 0px;}
.entry {
width: 220px;
float: left;
margin: 10px;
height: 198px;
background-image: url("images/shadow.png");
background-repeat: no-repeat;
background-position: bottom;}
figure {
display: block;
width: 202px;
height: 170px;
background-color: #e7e3d8;
padding: 9px;
text-align: left;}
figure img {
width: 200px;
height: 150px;
border: 1px solid #d6d6d6;}
figcaption {
background-image: url("images/icon.png");
padding-left: 20px;
background-repeat: no-repeat;}
</style>
```

* Summary 

* You can specify the dimensions 
of images using CSS.
This is very helpful when you use the same sized
images on several pages of your site.
* Images can be aligned both horizontally and vertically
using CSS.
* You can use a background image behind the box
created by any element on a page.
* Background images can appear just once or be
repeated across the background of the box.
* You can create image rollover effects by moving the
background position of an image.
* To reduce the number of images your browser has to
load, you can create image sprites.

-----

# Chapter 19: “Practical Information” (476-492)

* Summary

* Search engine optimization helps visitors find your
sites when using search engines.
* Analytics tools such as Google Analytics allow you to
see how many people visit your site, how they find it,
and what they do when they get there.
* To put your site on the web, you will need to obtain
domain name and web hosting.
* FTP programs allow you to transfer files from your
local computer to your web server.
* Many companies provide platforms for blogging, email
newsletters, e-commerce and other popular website
tools (to save you writing them from scratch).

# Chapter 9: pages 201-206 only. Flash is no longer supported by many browsers but is an important part of history

* SELECTING ELEMENTS
USING ID ATTRIBUTES

> get El ementByid () al lows you
to select a single element node
by specifying the value of its
id attribute.
This method has one parameter:
the value of the id attribute on
the element you want to select.
This value is placed inside quote
marks because it is a string. The
quotes can be single or double
quotes, but they must match.
In the example on the left, the
first line of JavaScript code finds
the element whose id attribute
has a value of one, and stores
a reference to that node in a
variable ca lled e 1.
The code then uses a property
called cl assName (which you
meet on p232) to update the
value of the cl ass attribute
of the element stored in this
variable. Its value is coo 1, and
this triggers a new rule in the
CSS that sets the background
color of the element to aqua.
Note how the c 1 assName
property is used on the variable
that stores the reference to the
element.
Browser Support: This is one of
the oldest and best supported
methods for accessing elements.

```html
<hl id="header">List King<lhl>
<h2>Buy groceries<lh2>
<ul>
<li id="one" class="hot"><em>fresh<lem>
figs<lli>
<li id="two" class="hot">pine nut s<lli>
<li id="three" class="hot">honey<lli>
<li id="four">balsamic vi negar<ll i>
</ul>
```

```js
II Select the element and store it in a variable.
var el = document.getElementByid('one');
II Change the value of the class attribute.
el.className ='cool ' ;
```

* SELECTING AN ELEMENT
FROM A NODELIST

> There are two ways to select an element from a Nodelist:
The item() method and array syntax.
Both require the index number of the element you want.
THE ;tern{) METHOD
Nodelists have a method
called item() which will return
an individual node from the
Node list.
You specify the index number
of the element you want as a
parameter of the method (inside
the parentheses).
Executing code when there are
no elements to work with wastes
resources. So programmers
often check that there is at least
one item in the Nodelist before
running any code. To do this,
use the 1 ength property of the
Nodelist - it tells you how many
items the Nodelist contains.
Here you can see that an if
statement is used. The condition
for the if statement is whether
the 1 ength property of the
Nodelist is greater than zero.
If it is, then the statements inside
the if statement are executed.
If not, the code continues to run
after the second curly brace

```js
var elements = document.getElementsByClassName('hot')
if (elements.length>= 1) {
var firstltem = elements.item(O);
}
```