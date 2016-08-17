# totorojs/totoro

### 简单易用、稳定的跨浏览器测试工具。



> github地址： https://github.com/totorojs/totoro  

> Star: 521  
> Fork: 100  
> Watch: 52    
> 以上截止到2016.08.17

### 特性

> 在真实的浏览器中运行  
> 支持所有的测试框架  
> 自动测试覆盖率  
> 足够健壮，可用于实战  


### 命令行配置项

-R, --runner

运行测试必须的数据，通常为本地文件路径或 URL。

默认：自动查找当前目录，tests 或 test 子目录下的 runner.html 或 index.html 均可被识别。

---

-C, --code

方便的 debug 途径。接受 单个 表达式、 JS 文件和 URL。totoro 将返回指定表达式计算的值或 JS 文件中所有 console.log() 输出结果。例如：

```
$ totoro --code document.body
$ totoro --code "console.log(document.body)"
$ totoro --code examples/code/code.js  // 我们真的准备了这个例子，试试看！
注意： --code 和 --runner 是互斥的选项！
```


---


-l, --labors

指定要运行测试的的应用名称，通常为浏览器，多个以逗号分隔。例如：

chrome,firefox,safari,ie  //不指定版本
ie/6,ie/7,ie/8,ie/9  //指定版本
默认：自动选取测试服务端可用的桌面浏览器。

-a, --adapter

测试框架的适配器，用于发送测试报告。接受内置关键字、本地路径和 URL。

已支持的内置关键字有：mocha, jasmine。

如指定为 no，则 totoro 不会尝试探测和插入适配器，认为用户会自行加载。

自定义适配器写法可参考 static/adapters/mocha.js。

默认：如果 --runner 指定的是本地路径，则会先查看 runner 所在的位置是否有 totoro-adapter.js；如果没找到或者 --runner 指定的是 url 则 totoro-server 会自动扫描 --runner 的内容尝试查找匹配的内置关键字。


---

-O, --root

如果 --runner 是一个本地文件，totoro 在测试时会起一个临时的 HTTP 服务，该选项指定这个服务的根目录，接受相对路径和绝对路径。

参见更多详情

默认：根据 --runner 和 --adapter 进行猜测。

-H, --host

测试服务 host。

默认：阿里的内部host

-P, --port

测试服务 port。

默认：9999

--no-proxy

不对 runner 指定的 URL 进行域名转换

默认：false

--no-coverage

跳过代码覆盖率检查.

默认：false

3.2 totoro list

显示当前可用的测试浏览器。配置项可通过 totoro list -h 查看。

