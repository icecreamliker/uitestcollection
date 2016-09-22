# angular/protractor

> github：https://github.com/angular/protractor    
> 
> Star: 5855  
> Fork: 1346  
> Watch: 400    
> Up to 2016.09.22


### What is protractor?

Protractor is an end-to-end test framework for AngularJS applications. Protractor is a Node.js program built on top of WebDriverJS. Protractor runs tests against your application running in a real browser, interacting with it as a user would.

### Features

* Test Like a User    
  Protractor is built on top of WebDriverJS, which uses native events and browser-specific drivers to interact with your application as a user would.    
* For AngularJS Apps    
  Protractor supports Angular-specific locator strategies, which allows you to test Angular-specific elements without any setup effort on your part.    

* Automatic Waiting    
  You no longer need to add waits and sleeps to your test. Protractor can automatically execute the next step in your test the moment the webpage finishes pending tasks, so you don’t have to worry about waiting for your test and webpage to sync.    

### How to write a test?

```javascript
describe('angularjs homepage todo list', function() {
  it('should add a todo', function() {
    browser.get('https://angularjs.org');

    element(by.model('todoList.todoText')).sendKeys('write first protractor test');
    element(by.css('[value="add"]')).click();

    var todoList = element.all(by.repeater('todo in todoList.todos'));
    expect(todoList.count()).toEqual(3);
    expect(todoList.get(2).getText()).toEqual('write first protractor test');

    // You wrote your first test, cross it off the list
    todoList.get(2).element(by.css('input')).click();
    var completedAmount = element.all(by.css('.done-true'));
    expect(completedAmount.count()).toEqual(2);
  });
});
```

The `describe` and `it` syntax is from the Jasmine framework. `browser` is a global created by Protractor, which is used for browser-level commands such as navigation with `browser.get`.