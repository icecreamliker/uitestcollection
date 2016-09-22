# gotwarlost/istanbul

> github：https://github.com/gotwarlost/istanbul    
> 
> Star: 5053  
> Fork: 516  
> Watch: 138    
> Up to 2016.09.22


### What is istanbul?

Yet another JS code coverage tool that computes statement, line, function and branch coverage with module loader hooks to transparently add coverage when running tests. Supports all JS coverage use cases including unit tests, server side functional tests and browser tests. Built for scale.

### Features

* All-javascript instrumentation library that tracks statement, branch, and function coverage.
* Module loader hooks to instrument code on the fly
* Command line tools to run node unit tests "with coverage turned on" and no cooperation whatsoever from the test runner
* Multiple report formats: HTML, LCOV, Cobertura and more.
* Ability to use as middleware when serving JS files that need to be tested on the browser.
* Can be used on the command line as well as a library
* Based on the awesome esprima parser and the equally awesome escodegen code generator
* Well-tested on node (prev, current and next versions) and the browser (instrumentation library only)

### Use cases

Supports the following use cases and more

* transparent coverage of nodejs unit tests
* instrumentation/ reporting of files in batch mode for browser tests
* Server side code coverage for nodejs by embedding it as custom middleware
