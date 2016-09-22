# jasmine/jasmine

> github：https://github.com/jasmine/jasmine    
> 
> Star: 11579  
> Fork: 1779  
> Watch: 493    
> Up to 2016.09.21


### A JavaScript Testing Framework

Jasmine is a Behavior Driven Development testing framework for JavaScript. It does not rely on browsers, DOM, or any JavaScript framework. Thus it's suited for websites, Node.js projects, or anywhere that JavaScript can run.

### Installation

For the Jasmine NPM module:    

https://github.com/jasmine/jasmine-npm

For the Jasmine Ruby Gem:    

https://github.com/jasmine/jasmine-gem

For the Jasmine Python Egg:    

https://github.com/jasmine/jasmine-py

For the Jasmine headless browser gulp plugin:    

https://github.com/jasmine/gulp-jasmine-browser

__To install Jasmine standalone on your local box:__

* Download the standalone distribution for your desired release from the releases page    

* Create a Jasmine directory in your project - `mkdir my-project/jasmine`    

* Move the dist to your project directory - `mv jasmine/dist/jasmine-standalone-2.0.0.zip my-project/jasmine`    

* Change directory - `cd my-project/jasmine`    

* Unzip the dist - `unzip jasmine-standalone-2.0.0.zip`   

__Add the following to your HTML file:__

```html
<link rel="shortcut icon" type="image/png" href="jasmine/lib/jasmine-2.0.0/jasmine_favicon.png">
<link rel="stylesheet" type="text/css" href="jasmine/lib/jasmine-2.0.0/jasmine.css">

<script type="text/javascript" src="jasmine/lib/jasmine-2.0.0/jasmine.js"></script>
<script type="text/javascript" src="jasmine/lib/jasmine-2.0.0/jasmine-html.js"></script>
<script type="text/javascript" src="jasmine/lib/jasmine-2.0.0/boot.js"></script>
```

#### Supported environments

Jasmine tests itself across many browsers (Safari, Chrome, Firefox, PhantomJS, and new Internet Explorer) as well as node. 
