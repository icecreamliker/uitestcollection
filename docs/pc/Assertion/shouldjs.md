# shouldjs/should.js

> github：https://github.com/tj/should.js    
> 
> Star: 2430  
> Fork: 211  
> Watch: 69    
> Up to 2016.09.22


### What is should.js?

_should_ is an expressive, readable, framework-agnostic assertion library. The main goals of this library are __to be expressive__ and __to be helpful__. It keeps your test code clean, and your error messages helpful.

By default (when you `require('should')`) _should_ extends the `Object.prototype` with a single non-enumerable getter that allows you to express how that object should behave. It also returns itself when required with `require`.

It is also possible to use should.js without getter (it will not even try to extend Object.prototype), just `require('should/as-function')`. Or if you already use version that auto add getter, you can call `.noConflict` function.

**Results of `(something).should` getter and `should(something)` in most situations are the same**

## Example
```javascript
var should = require('should');

var user = {
    name: 'tj'
  , pets: ['tobi', 'loki', 'jane', 'bandit']
};

user.should.have.property('name', 'tj');
user.should.have.property('pets').with.lengthOf(4);

// If the object was created with Object.create(null)
// then it doesn't inherit `Object.prototype`, so it will not have `.should` getter
// so you can do:
should(user).have.property('name', 'tj');

// also you can test in that way for null's
should(null).not.be.ok();

someAsyncTask(foo, function(err, result){
  should.not.exist(err);
  should.exist(result);
  result.bar.should.equal(foo);
});
```

### Assertions
#### chaining assertions

Every assertion will return a `should.js`-wrapped Object, so assertions can be chained.
To help chained assertions read more clearly, you can use the following helpers anywhere in your chain: `.an`, `.of`, `.a`, `.and`, `.be`, `.have`, `.with`, `.is`, `.which`. Use them for better readability; they do nothing at all.
For example:
```js
user.should.be.an.instanceOf(Object).and.have.property('name', 'tj');
user.pets.should.be.instanceof(Array).and.have.lengthOf(4);
```
Almost all assertions return the same object - so you can easy chain them. But some (eg: `.length` and `.property`) move the assertion object to a property value, so be careful.

#### Adding own assertions

Adding own assertion is pretty easy. You need to call `should.Assertion.add` function. It accept 2 arguments:

1. name of assertion method (string)
2. assertion function (function)

What assertion function should do. It should check only positive case. `should` will handle `.not` itself.
`this` in assertion function will be instance of `should.Assertion` and you **must** define in any way this.params object
 in your assertion function call before assertion check happen.

`params` object can contain several fields:

- `operator` - it is string which describe your assertion
- `actual` it is actual value, you can assume it is your own this.obj if you need to define you own
- `expected` it is any value that expected to be matched this.obj

You can assume its usage in generating AssertionError message like: expected `obj`? || this.obj not? `operator` `expected`?

In `should` sources appeared 2 kinds of usage of this method.

First not preferred and used **only** for shortcuts to other assertions, e.g how `.should.be.true()` defined:

```javascript
Assertion.add('true', function() {
    this.is.exactly(true);
});
```
There you can see that assertion function do not define own `this.params` and instead call within the same assertion `.exactly`
that will fill `this.params`. **You should use this way very carefully, but you can use it**.

Second way preferred and i assume you will use it instead of first.

```javascript
Assertion.add('true', function() {
    this.params = { operator: 'to be true', expected: true };

    should(this.obj).be.exactly(true);
});
```
in this case this.params defined and then used new assertion context (because called `.should`). Internally this way does not
 create any edge cases as first.

```javascript
Assertion.add('asset', function() {
    this.params = { operator: 'to be asset' };

    this.obj.should.have.property('id').which.is.a.Number();
    this.obj.should.have.property('path');
})

//then
> ({ id: '10' }).should.be.an.asset();
AssertionError: expected { id: '10' } to be asset
    expected '10' to be a number

> ({ id: 10 }).should.be.an.asset();
AssertionError: expected { id: 10 } to be asset
    expected { id: 10 } to have property path
```
