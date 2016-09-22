# sinonjs/sinon

> github：https://github.com/sinonjs/sinon    
> 
> Star: 3301  
> Fork: 449  
> Watch: 77    
> Up to 2016.09.22


### What is sinon?

Standalone test spies, stubs and mocks for JavaScript.
No dependencies, works with any unit testing framework.

### Goals

* No global pollution
* Easy to use
* Require minimal “integration”
* Easy to embed seamlessly with any testing framework
* Easily fake any interface
* Ship with ready-to-use fakes for XMLHttpRequest, timers and more

### It use just like this


* __Testing Ajax__

The following function triggers network activity:

```javascript
function getTodos(listId, callback) {
    jQuery.ajax({
        url: "/todo/" + listId + "/items",
        success: function (data) {
            // Node-style CPS: callback(err, data)
            callback(null, data);
        }
    });
}
```

To test this function without triggering network activity we could stub jQuery.ajax:

```javascript
after(function () {
    // When the test either fails or passes, restore the original
    // jQuery ajax function (Sinon.JS also provides tools to help
    // test frameworks automate clean-up like this)
    jQuery.ajax.restore();
});

it("makes a GET request for todo items", function () {
    sinon.stub(jQuery, "ajax");
    getTodos(42, sinon.spy());

    assert(jQuery.ajax.calledWithMatch({ url: "/todo/42/items" }));
});
```