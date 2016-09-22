# dalekjs/dalek

>github： https://github.com/dalekjs/dalek
>
>Star: 700  
>Fork: 66  
>Watch: 54    
>Up to 2016.08.17


### DalekJS is an open source UI testing tool written in JavaScript, it will:

> 1. launch & automate your browser
> 2. fill & submit forms
> 3. click & follow links
> 4. capture screenshots
> 5. run your functional tests
> 6. … and it works on Windows, Linux & Mac



### 写法：

```javascript
module.exports = {
'Page title is correct': function (test) {
  test
    .open('http://google.com')
    .assert.title().is('Google', 'It has title')
    .done();
}
};
```
then
```$ dalek test/my_first_test.js```

console
```
Running tests
Running Browser: Phantomjs
RUNNING TEST - "Page title is correct"
▶ OPEN http://google.com
✔ TITLE It has title
✔ 1 Assertions run
✔ TEST - "Page title is correct" SUCCEEDED
1/1 assertions passed. Elapsed Time: 2 sec
```



