# pivotal/cedar
> github： https://github.com/pivotal/cedar

> Star: 1088  
> Fork: 151      
> Watch: 65    
> Up to 2016.08.23    

### What is cedar?
##### Cedar, BDD style testing for Objective-C and Swift
Cedar is a self-contained behavior driven development (BDD) framework for Objective-C and Swift. It provides improvements in clarity and better organizational facilities than the tools provided by XCTest/OCUnit. In environments where C++ is available, it also provides powerful built-in matchers, test doubles and fakes.

### Objective-C:

```ObjC
describe(@"Cedar", ^{
    it(@"is great for testing Objective-C code", ^{
        yourTests should be_clearer();
    });
});
```
### Swift:
```Swift
class CedarSpec: CDRSpec {
    override func declareBehaviors() {
        describe("Cedar") {
            it("also works great with Swift") {
                expect(yourTests).to(beClearer())
            }
        }
    }
}
```

### Cedar Wiki

https://github.com/pivotal/cedar/wiki