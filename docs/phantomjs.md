# ariya/phantomjs
> github地址： https://github.com/ariya/phantomjs

> Star: 19126  
> Fork: 3957      
> Watch: 997    
> 以上截止到2016.08.17  

## Full web stack No browser required

PhantomJS is a headless WebKit scriptable with a JavaScript API. It has fast and native support for various web standards: DOM handling, CSS selector, JSON, Canvas, and SVG.  

## PhantomJS is an optimal solution for

#### 1. HEADLESS WEBSITE TESTING
Run functional tests with frameworks such as Jasmine, QUnit, Mocha, Capybara, WebDriver, and many others. 
#### 2. SCREEN CAPTURE
Programmatically capture web contents, including SVG and Canvas. Create web site screenshots with thumbnail preview. 
#### 3. PAGE AUTOMATION
Access and manipulate webpages with the standard DOM API, or with usual libraries like jQuery. 
#### 4. NETWORK MONITORING
Monitor page loading and export as standard HAR files. Automate performance analysis using YSlow and Jenkins. 

#### PhantomJS is used in the test workflow of various open-source projects:
Bootstrap, CodeMirror, Ember.js, jQuery Mobile, Less.js, Modernizr, YUI3, and many more.

```
// Simple Javascript example

console.log('Loading a web page');
var page = require('webpage').create();
var url = 'http://phantomjs.org/';
page.open(url, function (status) {
  //Page is loaded!
  phantom.exit();
});
```