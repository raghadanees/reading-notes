## Audio, Video, Images

- *You can control the size of an image using the width and height properties in CSS*
- *In order to center an image, it should be turned into a blocklevel element using the display property with a value of block.*

img.align-center {

display: block ;

margin: 0px auto ; 
}

- The background-image property allows you to place an image behind any HTML element. This could be the entire page or just part of the page. By default, a background image will repeat to fill the entire box.

body {

background-image: url("images/pattern.gif");
}

or

p {

background-image: url("images/pattern.gif");
}
- background-position
*When an image is not being repeated, you can use the background-position property to specify where in the browser window the background image should be placed.*


