# azer/prova

> github：https://github.com/azer/prova    
> 
> Star: 321  
> Fork: 26  
> Watch: 10    
> Up to 2016.09.21

### prova

Node & Browser Test runner based on Tape and Browserify.

Screencasts: node.gif, browser.gif, both.gif, headless browser

Slides: http://slides.com/azer/prova

### Features and screenshots:

* Embeds Tape
* Comes with a builtin web app to run tests on browser, sourcemaps are enabled.
* Outputs less when tests pass (Node, Browser)
* Outputs more when tests fail (Node, Browser)
* Browser app runs tests inside of an iframe Screenshot
* Uses watchify to observe file changes and restart browser tests. GIF Screenshot
* Lets filtering test cases (e.g node test.js -g foobar)
* Comes with browser-launcher for launching browsers automatically and headless testing. (Screenshot)
* Clickable error stacks on the browser: Screenshot
* Optional progress bar for slow tests. GIFs: Node / Browser

### Install

`$ npm install -g azer/prova`

### Usage

#### Example test:
```javascript
var test = require('prova')

test('timing test', function (t) {
  t.plan(2)

  t.equal(typeof Date.now, 'function')
  var start = Date.now()

  setTimeout(function () {
    t.equal(Date.now() - start, 100)
  }, 100)
})
```

#### In Node, it will output:
```javascript
$ node test.js
Passed 1 test.
```

#### In Browser

To run the tests in a web browser, just pass -b parameter:

`$ node test.js -b`    

Visit localhost:7559 with a browser to start running the tests.
