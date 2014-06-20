SVGEjector
==========

A (to-be-maybe) fast, dynamic inline SVG-to-fallback DOM injection library/polyfill. Inspired by [SVGInjector](https://github.com/iconic/SVGInjector). I've rapidly put this library together using parts of [Waybury](http://waybury.com/)'s SVGInjector repository and the overall JavaScript architecture from [Picturefill](https://github.com/scottjehl/picturefill).

## Why?
There are a number of ways to use SVG on a page (`object`, `embed`, `iframe`, `img`, CSS `background-image`) but to unlock the full potential of SVG, including full element-level CSS styling and evaluation of embedded JavaScript, the full SVG markup must be included directly in the DOM.

Most modern browsers support SVG and inline-SVG without issue. But we aren't taking full advantage of it because most often we need to drag along--kicking and screaming sometimes--the older generation that don't support scalable vector graphics.

Wrangling and maintaining a bunch of inline SVG on your pages isn't anyone's idea of good time, so **SVGInjector** lets you work with simple `img` tag elements (or other tag of your choosing) and does the heavy lifting of swapping in the SVG markup inline for you.

But why make the modern browsers do all the swapping for some sexy vector graphics. Let those old farts do the hard work to get what they want.

So, for those that do enjoy a hot mess of XML or have mastered some form of [icon system](http://css-tricks.com/svg-sprites-use-better-icon-fonts/), **SVGEjector** lets you focus on your SVG elements and does the work of swapping your SVG for IMG, or other, markup inline for you.

## How?
* Any SVG element, DOM element with an SVG file, or array of elements, passed to **SVGEjector** will be replaced with IMG or SPAN elements inline.
* Any embedded JavaScript in the SVG will optionally be extracted, cached and evaluated.
