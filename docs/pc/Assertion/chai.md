# chaijs/chai

> github：https://github.com/chaijs/chai    
> 
> Star: 3337  
> Fork: 311  
> Watch: 95    
> Up to 2016.09.22


### What is chai?

Chai is a BDD / TDD assertion library for node and the browser that can be delightfully paired with any javascript testing framework.

### Features

Chai has several interfaces that allow the developer to choose the most comfortable. The chain-capable BDD styles provide an expressive language & readable style, while the TDD assert style provides a more classical feel.
    

* __Should__    
       
       
  ```javascript
  chai.should();

  foo.should.be.a('string');
  foo.should.equal('bar');
  foo.should.have.length(3);
  tea.should.have.property('flavors')
    .with.length(3);
  ```
    

* __Expect__    
    

  ```javascript
  var expect = chai.expect;

  expect(foo).to.be.a('string');
  expect(foo).to.equal('bar');
  expect(foo).to.have.length(3);
  expect(tea).to.have.property('flavors')
    .with.length(3);
  ```
    

* __Assert__    
    

  ```javascript
  var assert = chai.assert;

  assert.typeOf(foo, 'string');
  assert.equal(foo, 'bar');
  assert.lengthOf(foo, 3)
  assert.property(tea, 'flavors');
  assert.lengthOf(tea.flavors, 3);
  ```

### Related Projects

- [chaijs / chai-docs](https://github.com/chaijs/chai-docs): The chaijs.com website source code.
- [chaijs / assertion-error](https://github.com/chaijs/assertion-error): Custom `Error` constructor thrown upon an assertion failing.
- [chaijs / deep-eql](https://github.com/chaijs/deep-eql): Improved deep equality testing for Node.js and the browser.
- [chaijs / type-detect](https://github.com/chaijs/type-detect): Improved typeof detection for Node.js and the browser.
- [chaijs / check-error](https://github.com/chaijs/check-error): Error comparison and information related utility for Node.js and the browser.
- [chaijs / loupe](https://github.com/chaijs/loupe): Inspect utility for Node.js and browsers.
- [chaijs / pathval](https://github.com/chaijs/pathval): Object value retrieval given a string path.