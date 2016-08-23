# theintern/intern

> github： https://github.com/theintern/intern

> Star: 3487    
> Fork: 267         
> Watch: 142      
> Up to 2016.08.17  
> 


### What is intern?

Intern is a complete test system for JavaScript designed to help you write and run consistent, high-quality test cases for your JavaScript libraries and applications. It can be used to test any JavaScript code. It can even be used to test non-JavaScript Web and mobile apps, and to run tests written for other test systems.

If you’re into name-dropping, Intern gets used every day by teams at Twitter, Stripe, Mozilla, IBM, Marriott, Philips, Zenput, Alfresco, Esri, HSBC, ING, Intuit, and more. It’s also the testing framework of choice for growing numbers of open-source projects.

### Quick start

* ##### Install from npm

```
cd /my/project/root
npm install intern --save-dev
```

* ##### Create a copy of the [example configuration file](https://github.com/theintern/intern/blob/master/tests/example.intern.js) in your package’s test directory and edit appropriately. See the[configuration documentation](https://theintern.github.io/intern/#common-config) for a list of all available options.

```
mkdir tests ; cp node_modules/intern/tests/example.intern.js tests/intern.js
```

* ##### Verify your configuration works by running the Node.js client and seeing that no errors are output.

```
node_modules/.bin/intern-client config=tests/intern
```

* ##### Start writing tests! 

```javascript
define(function (require) {
  var registerSuite = require('intern!object');
  var assert = require('intern/chai!assert');

  var request = require('request');

  registerSuite({
    name: 'async demo',

    'async test': function () {
      var dfd = this.async(1000);

      request(
        'http://example.com/test.txt',
        dfd.callback(function (error, data) {
          if (error) {
            throw error;
          }

          assert.strictEqual(data, 'Hello world!');
        })
      );
    }
  });
});
```
In this example, an HTTP request is made using a hypothetical request library that uses legacy Node.js-style callbacks. When the call is completed successfully, the data is checked to make sure it is correct.

If the data is correct, the Promise associated with dfd will be resolved, and the test will pass; otherwise, it will be rejected (because an error is thrown), and the test will fail.

---
read More:    
http://www.ibm.com/developerworks/cn/web/1412_zhongsq_intern/
