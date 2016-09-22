# alex-seville/blanket

> github：https://github.com/alex-seville/blanket    
> 
> Star: 1286  
> Fork: 180  
> Watch: 42    
> Up to 2016.09.22


### What is blanket?

blanket.js is a simple code coverage library for javascript. Designed to be easy to install and use, for both browser and nodejs.

### Philosophy

Blanket.js is a code coverage tool for javascript that aims to be:

* Easy to install
* Easy to use
* Easy to understand
Blanket.js can be run seamlessly or can be customized for your needs.

### Mechanism

JavaScript code coverage compliments your existing JavaScript tests by adding code coverage statistics (which lines of your source code are covered by your tests).

Blanket works in a 3 step process:

* Loading your source files
* Parsing the code using Esprima and node-falafel, and instrumenting the file by adding code tracking lines.
* Connecting to hooks in the test runner to output the coverage details after the tests have completed.

