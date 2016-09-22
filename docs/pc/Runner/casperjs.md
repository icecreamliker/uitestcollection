# casperjs/casperjs

>github： https://github.com/casperjs/casperjs
>
>Star: 5978  
>Fork: 945  
>Watch: 287    
>Up to 2016.09.22

### CasperJS

CasperJS is a navigation scripting & testing utility for [PhantomJS](http://www.phantomjs.org/)
and [SlimerJS](http://slimerjs.org/) (still experimental).
It eases the process of defining a full navigation
scenario and provides useful high-level functions, methods & syntactic sugar for doing common
tasks such as:

- defining & ordering [navigation steps](http://docs.casperjs.org/en/latest/quickstart.html)
- [filling forms](http://docs.casperjs.org/en/latest/modules/casper.html#fill)
- [clicking links](http://docs.casperjs.org/en/latest/modules/casper.html#click)
- [capturing screenshots](http://docs.casperjs.org/en/latest/modules/casper.html#captureselector) of a page (or an area)
- [making assertions on remote DOM](http://docs.casperjs.org/en/latest/modules/tester.html)
- [logging](http://docs.casperjs.org/en/latest/logging.html) & [events](http://docs.casperjs.org/en/latest/events-filters.html)
- [downloading](http://docs.casperjs.org/en/latest/modules/casper.html#download) resources, even binary ones
- catching errors and react accordingly
- writing [functional test suites](http://docs.casperjs.org/en/latest/testing.html), exporting results as JUnit XML (xUnit)

Browse the [sample examples repository](https://github.com/casperjs/casperjs/tree/master/samples).
Don't hesitate to pull request for any cool example of yours as well!

**Read the [full documentation](http://docs.casperjs.org/) on casperjs documentation website.**

Subscribe to the [project mailing-list](https://groups.google.com/forum/#!forum/casperjs)

Follow the CasperJS project [on twitter](https://twitter.com/casperjs_org) and [Google+](https://plus.google.com/b/106641872690063476159/).

## Show me some code!

First [install CasperJS](http://docs.casperjs.org/en/latest/installation.html), we'll use 1.1 beta here.

Sample test to see if some dropdown can be opened:

```javascript
casper.test.begin('a twitter bootstrap dropdown can be opened', 2, function(test) {
    casper.start('http://getbootstrap.com/2.3.2/javascript.html#dropdowns', function() {
        test.assertExists('#navbar-example');
        this.click('#dropdowns .nav-pills .dropdown:last-of-type a.dropdown-toggle');
        this.waitUntilVisible('#dropdowns .nav-pills .open', function() {
            test.pass('Dropdown is open');
        });
    }).run(function() {
        test.done();
    });
});
```

Run the script:

![](http://cl.ly/image/271e2i403A0F/Capture%20d%E2%80%99%C3%A9cran%202013-01-20%20%C3%A0%2009.26.15.png)

##Support

**Help request**. If you're stuck using CasperJS and don't understand how to achieve something, please [ask on the mailing-list](https://groups.google.com/forum/#!forum/casperjs) first. If the discussion reveals that you have found a real issue that might need a change within CasperJS, file an issue.

**Filing issues**. It takes a lot of time to review, validate, and de-duplicate filed issues. This time could be spent better on actually improving on CasperJS. Filing an issue might be a helpful contribution, but we expect you to read our [CONTRIBUTING.md](https://github.com/casperjs/casperjs/blob/master/CONTRIBUTING.md) guidelines first. 

**Professional Support**. Need help with getting CasperJS up and running? Got a time-consuming problem you want to get solved quickly?

Try to find someone to address your specific problem and [post a reward at bountysource](https://www.bountysource.com).

If you need to have a known issue resolved and don't have the time or skills to do it on your own, you could [post a reward for any open issue directly](https://www.bountysource.com/teams/casperjs/issues).