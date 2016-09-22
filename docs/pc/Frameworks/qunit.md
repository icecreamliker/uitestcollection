# jquery/qunit

> github：https://github.com/jquery/qunit    
> 
> Star: 3529  
> Fork: 724  
> Watch: 149    
> Up to 2016.09.21

### QUnit - A JavaScript Unit Testing Framework.

QUnit is a powerful, easy-to-use, JavaScript unit testing framework. It's used by the jQuery project to test its code and plugins but is capable of testing any generic JavaScript code (and even capable of testing JavaScript code on the server-side).

QUnit is especially useful for regression testing: Whenever a bug is reported, write a test that asserts the existence of that particular bug. Then fix it and commit both. Every time you work on the code again, run the tests. If the bug comes up again - a regression - you'll spot it immediately and know how to fix it, because you know what code you just changed.

Having good unit test coverage makes safe refactoring easy and cheap. You can run the tests after each small refactoring step and always know what change broke something.

QUnit is similar to other unit testing frameworks like JUnit, but makes use of the features JavaScript provides and helps with testing code in the browser, e.g. with its stop/start facilities for testing asynchronous code.

### Development

To submit patches, fork the repository, create a branch for the change. Then implement the change, run `npm test` to lint and test it, then commit, push and create a pull request.

Include some background for the change in the commit message and `Fixes #nnn`, referring to the issue number you're addressing.

To run `npm test`, you need Node.js, which includes `npm`.

### A minimal QUnit test setup:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>QUnit Example</title>
  <link rel="stylesheet" href="https://code.jquery.com/qunit/qunit-2.0.1.css">
</head>
<body>
  <div id="qunit"></div>
  <div id="qunit-fixture"></div>
  <script src="https://code.jquery.com/qunit/qunit-2.0.1.js"></script>
  <script src="tests.js"></script>
</body>
</html>
```

```javascript
QUnit.test( "hello test", function( assert ) {
  assert.ok( 1 == "1", "Passed!" );
});
```