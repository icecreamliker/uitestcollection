# kif-framework/KIF
> github： https://github.com/kif-framework/KIF

> Star: 4362  
> Fork: 734      
> Watch: 189    
> Up to 2016.08.22

### What is KIF?

KIF, which stands for Keep It Functional, is an iOS integration test framework. It allows for easy automation of iOS apps by leveraging the accessibility attributes that the OS makes available for those with visual disabilities.    

KIF builds and performs the tests using a standard XCTest testing target. Testing is conducted synchronously in the main thread (running the run loop to force the passage of time) allowing for more complex logic and composition. This also allows KIF to take advantage of the Xcode 5 Test Navigator, command line build tools, and Bot test reports. Find out more about Xcode 5 features.    

KIF uses undocumented Apple APIs. This is true of most iOS testing frameworks, and is safe for testing purposes, but it's important that KIF does not make it into production code, as it will get your app submission denied by Apple. Follow the instructions below to ensure that KIF is configured correctly for your project.    

### Features

##### Minimizes Indirection

All of the tests for KIF are written in Objective C. This allows for maximum integration with your code while minimizing the number of layers you have to build.

##### Easy Configuration

KIF integrates directly into your Xcode project, so there's no need to run an additional web server or install any additional packages.

##### Wide OS coverage

KIF's test suite has been run against iOS 5.1 and above (including iOS 9), though lower versions will likely work.

##### Test Like a User

KIF attempts to imitate actual user input. Automation is done using tap events wherever possible.

##### Automatic Integration with Xcode 5 Testing Tools

Xcode 5 introduces new testing and continuous integration tools built on the same testing platform as KIF. You can easily run a single KIF test with the Test Navigator or kick off nightly acceptance tests with Bots.






