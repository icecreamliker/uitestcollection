# laurentj/slimerjs

>github： https://github.com/laurentj/slimerjs
>
>Star: 1973  
>Fork: 204  
>Watch: 93    
>Up to 2016.09.22


# SlimerJS
http://slimerjs.org/

SlimerJS is a scriptable browser. It allows you to manipulate a web page
with an external Javascript script: opening a webpage, clicking on links, modifying the content...
It is useful to do functional tests, page automation, network monitoring, screen capture etc.

It is a tool like [PhantomJs](http://phantomjs.org/), except that
it runs Gecko instead of Webkit, and it is not (yet) natively headless.
However, it can be headless with the use of xvfb under Linux or MacOS.

SlimerJS provides the same API of PhantomJS. The current version of SlimerJS
is highly compatible with PhantomJS 1.9.
See current release notes in docs/release-notes-*.rst, and
read the [compatibility table](https://github.com/laurentj/slimerjs/blob/master/API_COMPAT.md)
to know the implementation level.

The main goal of SlimerJS is to allow to execute all scripts developed for PhantomJS. So
you could use tools like [CasperJS](http://casperjs.org). In fact, CasperJs 1.1 and higher
can be executed with SlimerJS!

SlimerJS is not only a PhantomJS clone, it contains also [additional features](http://slimerjs.org/features.html).

Technically, SlimerJS is a XUL/JS application that is launched with
Firefox.