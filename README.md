# bootstrap-sass-rem-boilerplate
Boilerplate setup of SASS Bootstrap + Compass using `rem` as the base unit instead of `px`.  This also has sensible defaults added to give a strong vertical rhythm to your typography, to go nicely with Bootstrap's grid.  This can be adapted for use with `em` instead of `rem`.

## Included libraries

In addition to the basic boilerplate, we've added a few optional things you should feel free to remove:

* [Compass](http://compass-style.org/) - extra mixins and tools for Sass.
* [Sass Web Fonts](https://github.com/penman/Sass-Web-Fonts) - font loader for Google Fonts.
* [Breakpoint](https://github.com/at-import/breakpoint) - breakpoints for Sass.
* [Font Awesome](http://fortawesome.github.io/Font-Awesome/) - replaces the default Glypicons from Bootstrap with extra icons.

This package is built with the following tools:

* [Bower](http://bower.io/)
* [Sass](http://sass-lang.com/)
* [Bootstrap](http://getbootstrap.com/) (specifically, [bootstrap-sass](https://github.com/twbs/bootstrap-sass))
* [Gridlover](http://www.gridlover.net/app/) - used to generate our baseline vertical rhythm.


## Installation

0. Install [bower](http://bower.io/#install-bower), [sass](http://sass-lang.com/install), and [compass](http://compass-style.org/install/).
1. Run `bower install`
2. Build the css with `compass compile`, or watch for local changes and continuously re-build with `compass watch`.

## Usage

Here are the basic files you'll want to modify:

* The main loader file is [./sass/style.scss](./sass/style.scss).  Add links to your style files here.
* Global variables for the system are in [./sass/config/_settings.scss](./sass/config/_settings.scss).
* The bootstrap-specific variables are kept in [./sass/config/_bootstrap-settings.scss](./sass/config/_bootstrap-settings.scss).
* There's a duplicate of the base bootstrap variable files, setup for use with `rem` in [./sass/mixins/_bootstrap-variables.scss](./sass/mixins/_bootstrap-variables.scss)
* The replacement for the default bootstrap loader file in [./sass/mixins/_bootstrap-minimal.scss](./sass/mixins/_bootstrap-minimal.scss) - you should comment out packages you're not using from this file.

Other things in this package:

* [A library to override some of the hardcoded problems bootstrap has for vertical rhythm.](./sass/mixins/_bootstrap-overrides.scss)
* [A helper to convert px to em.](./sass/mixins/_em.scss)
* [Bootstrap's default examples ported to work a 2rem line height.](./examples/)  These aren't designed to be pixel-perfect, just guidelines for reference.
