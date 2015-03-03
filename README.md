# Bootstrap grid with Sass, and much more  [![Gem Version](https://badge.fury.io/rb/bootstrap-sass.svg)](http://badge.fury.io/rb/bootstrap-sass)


Bootstrap-grid with Sass is a derived portion of Bootstrap Sass, which includes only bootstrap-grid, responsive utility, and own helper functions, which makes the templating process easier and faster, without the complications of compiling a new bootstrap configuration, and without the uneccessarys resource it provides.

## Installation

* For Sass users, make sure you have compass, copy what is in `sass` folder, you can use the provided style.scss for starting the project, or can just simply import in your own style.scss: 
```scss 
@import config;
@import bootstrap;
```
* For CSS users, include your css file before other stylings. Yes it's that simple!
```html
<link rel="stylesheet" type="text/css" href="style.css">
```
## Configuration 

This is the best part, you can configure your settings directly in `config.scss`, it's so intuitive that I don't have to explain anything here. (Only for Sass user, do I need to remind about `compass watch`)
```scss
// Columns and gutter
$grid-columns: 24;
$grid-gutter-width: 20px;

// Max fixed width
$max-width: 1200px;

// Max-width / Container max-width
$max-width-lg: 95%; //1140px
$max-width-md: 95%; //942px
$max-width-sm: 95%; //729px
$max-width-xs: 95%; //456px

//Break points ~ Conventionally: $screen-size-max-width - 1
$break-xs: 479px; $break-sm: 767px; $break-md: 991px; $break-lg: 1199px;

// Normalize or helper
// @import 'bootstrap/helpers/normalize';
@import 'bootstrap/helpers/reset';
```

## Using 

* Container-fluid removed, I meant, why do we even...
* If you set `max-width: 1200px`, container will have `max-width: 1200px` and that's it, none of the padding crap. No more fight width designer
* Grid system and visible/hidden utility naming convention is still the same as Bootstrap CSS
* Extra
  * Put `wide` before any `col`, you get a column without the padding, i. e.  `.wide-col-xs-4`
  * `block-center`, `block-left`, `block-right`, `block-justify` does what it literally means. Add these class to the parent of the elements that you want to align. 

* A shortcut for media query, simply amazing. Imagine how much time you can save with this
```scss
@include ss((xs, sm, md, lg, xl)) {
  .toggle {
    margin-top: 1em; 
  }
}

//will become

@media (min-width: 1200px) and (max-width: 9999px) {
  .toggle {
    margin-top: 1em; 
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .toggle {
    margin-top: 1em; 
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .toggle {
    margin-top: 1em; 
  }
}
@media (min-width: 480px) and (max-width: 767px) {
  .toggle {
    margin-top: 1em; 
  }
}

@media (min-width: 0px) and (max-width: 479px) {
  .toggle {
    margin-top: 1em; 
  }
}
```
## Credits

* [Twitter Bootstrap](getbootstrap.com/css/)
* [Twitter Bootstrap Sass](https://github.com/twbs/bootstrap-sass)
* Inspiration from [G-Works Oy] (http://www.g-works.fi/)
* MIT License. For more information, open [LICENCE] (https://github.com/fuksi/bootstrap-grid-sass/blob/master/LICENSE)

## Contacts

This is my first open source project, it would be strange if nothing goes wrong, especially this documentation. Pleace contact me, if, for example, the license is not appropriate. (And yes I would be very happy if Twitter got here and previewed my repo.)

Phuc Tran
dinh.tran (at) metropolia.fi

## Enjoy!
