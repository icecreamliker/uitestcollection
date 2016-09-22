# facebook/jest

> github：https://github.com/facebook/jest    
> 
> Star: 5388  
> Fork: 656  
> Watch: 181    
> Up to 2016.09.21

### What is jest?

Jest is a JavaScript unit testing framework, used by Facebook to test services and React applications.

### Features

* __Adaptable__    
  Jest uses Jasmine assertions by default and Jest is modular, extendible and configurable.

* __Sandboxed and Fast__    
  Jest virtualizes JavaScript environments, provides browser mocks and runs tests in parallel across workers.

* __Snapshot Testing__    
  Jest can capture snapshots of React trees or other serializable values to write tests quickly and it provides a seamless update experience.

### Why use jest?

* Jest automatically finds tests to execute in your repo

* It sandboxes test files, and resets state automatically for every test.

* Jest allows you to test asynchronous code synchronously as well as Promises and async/await.

* Uses static analysis to find and only run relevant test files during local development.

* Runs your tests with a fake DOM implementation (via jsdom) on the command line.

* Runs tests in parallel processes to minimize test runtime.

* It works with any compile-to-JS language and integrates seamlessly with Babel.

* Jest provides a manual mocking library. And it creates coverage reports.