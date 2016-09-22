# alibaba/macaca

>github： https://github.com/alibaba/macaca
>
>Star: 918  
>Fork: 133  
>Watch: 94    
>Up to 2016.08.23

### What is macaca?
Solution for Automation Test with Ease

### Features

* Both Mobile, Desktop Platforms Supported
* Native, Hybrid, Mobile Web Multi-applications Supported
* Command line tools & CI Solution provided

### Testcase

The BDD interface provides methods like: `describe()`, `it()`, `before()`, `after()`, `beforeEach()`, and `afterEach()`.
The snippet below is the recommended way to write your testcase.

```javascript
describe('Macaca test sample', function() {

  ...

  it('#1 should login successfully', function() {
    return driver
      .login('12345678', '111111')
      .sleep(1000);
  });

  ...

  it('#6 should works with web', function() {
    return driver
      .webview()
      .elementById('index-kw')
      .sendKeys('Macaca')
      .elementById('index-bn')
      .tap()
      .sleep(5000)
      .source()
      .then(function(html) {
        html.should.containEql('Macaca');
      })
      .takeScreenshot();
  });

  ...

});
```
