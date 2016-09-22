# nightwatchjs/nightwatch

>github： https://github.com/nightwatchjs/nightwatch
>
>Star: 5060  
>Fork: 451  
>Watch: 197    
>Up to 2016.09.22


### nightwatch

UI automated testing framework powered by Node.js. It uses the Selenium WebDriver API.

### Install Nightwatch

Install Node.js and then:

```bash
$ git clone https://github.com/nightwatchjs/nightwatch.git
$ cd nightwatch
$ npm install
```

### Run tests

The tests for Nightwatch are written using Mocha exports interface so they can also be run with Nightwatch itself.

To run the unit tests using mocha, do:
```bash
$ npm test
```

To run the unit tests using Nightwatch, do:

```bash
$ npm run unit-tests
```

To check test coverage, run the command:

```bash
$ npm run mocha-coverage
```

and then open the generate file coverage.html in your browser.

### Features

* __Clean syntax__    
    

Simple but powerful syntax which enables you to write tests very quickly, using only Javascript (Node.js) and CSS or Xpath selectors.    

* __Built-in test runner__    
    

Built-in command-line test runner which can run the tests either sequentially or in parallel, together, by group, tags or single. Grunt support is built-in.    
* __Selenium server__    
    

Controls the Selenium standalone server automatically in a separate child process; can be disabled if Selenium runs on another host.    
    
* __Cloud services support__    
    

Works with cloud testing providers, such as SauceLabs and BrowserStack.    

* __CSS & Xpath support__    
    
Either CSS or Xpath selectors can be used to locate and verify elements on the page or execute commands.    

* __Continous integration support__    
    

JUnit XML reporting is built-in so you can integrate your tests in your build process with systems such as Teamcity, Jenkins, Hudson etc.    


* __Easy to extend__    
    
    
Flexible command and assertion framework which makes it easy to extend to implement your application specific commands and assertions.


