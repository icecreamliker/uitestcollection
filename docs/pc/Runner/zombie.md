# assaf/zombie

>github： https://github.com/assaf/zombie
>
>Star: 4086  
>Fork: 447  
>Watch: 118    
>Up to 2016.09.22

### Zombie.js

Insanely fast, headless full-stack testing using Node.js

### The Bite

If you're going to write an insanely fast, headless browser, how can you not
call it Zombie?  Zombie it is.

Zombie.js is a lightweight framework for testing client-side JavaScript code in
a simulated environment.  No browser required.

Let's try to sign up to a page and see what happens:

```js
const Browser = require('zombie');

// We're going to make requests to http://example.com/signup
// Which will be routed to our test server localhost:3000
Browser.localhost('example.com', 3000);

describe('User visits signup page', function() {

  const browser = new Browser();

  before(function(done) {
    browser.visit('/signup', done);
  });

  describe('submits form', function() {

    before(function(done) {
      browser
        .fill('email',    'zombie@underworld.dead')
        .fill('password', 'eat-the-living')
        .pressButton('Sign Me Up!', done);
    });

    it('should be successful', function() {
      browser.assert.success();
    });

    it('should see welcome page', function() {
      browser.assert.text('title', 'Welcome To Brains Depot');
    });
  });
});
```

This example uses the [Mocha](https://github.com/mochajs/mocha) testing
framework, but Zombie will work with other testing frameworks.  Since Mocha
supports promises, we can also write the test like this:

```js
const Browser = require('zombie');

// We're going to make requests to http://example.com/signup
// Which will be routed to our test server localhost:3000
Browser.localhost('example.com', 3000);

describe('User visits signup page', function() {

  const browser = new Browser();

  before(function() {
    return browser.visit('/signup');
  });

  describe('submits form', function() {

    before(function() {
      browser
        .fill('email',    'zombie@underworld.dead')
        .fill('password', 'eat-the-living');
      return browser.pressButton('Sign Me Up!');
    });

    it('should be successful', function() {
      browser.assert.success();
    });

    it('should see welcome page', function() {
      browser.assert.text('title', 'Welcome To Brains Depot');
    });
  });

});
```

Well, that was easy.