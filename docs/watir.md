#watir/watir

> github地址： https://github.com/watir/watir

> Star: 637    
> Fork: 135         
> Watch: 67      
> 以上截止到2016.08.17  

### What is watir?

Watir Powered By Selenium!

What is an open source Ruby library for automating tests. Watir interacts with a browser the same way people do: clicking links, filling out forms and validating text.

### watir特性

Watir是一个轻量级的用于开发基于Web应用的自动化测试框架，它基于Ruby语言，提供了丰富的开发库，简化了自动化测试程序开发。下面我们总结了Watir的主要一些优良特性：

* Watir 基于 Ruby 语言。 Ruby 是面向对象语言，功能强大，简单易用。程序解释执行不用编译;

* Watir 支持多种操作系统平台，包括 Windows, Mac, Linux ;同时支持多种主流浏览器，如 IE, Firefox, Chrome

* Watir 提供了丰富的开发库，封装了包括浏览器窗口 windows，button, link, dialog, image, table, div 等绝大多数 HTML 对象类型，方便测试人员快速构建自动化测试程序。

* Ruby 提供了强大的交互命令工具 IRB(Interactive Ruby Shell), 在 Watir 程序开发中，我们使用 IRB 调试代码。别于传统调试方法，测试人员可以就单独一条命令或者一段程序进行调试，从而能够快速定位错误，节省调试时间。

* Ruby 提供了 Test::Unit 单元测试框架，通过继承该框架，我们可以对测试用例，测试用例集 (Test Suites) 进行灵活方便地组合和调用，并且可利用断言 (Assertion) 来验证测试结果。

* 其他脚本语言如 Perl, Python, Shell 等也可以很好地集成到 Watir 程序中。

* Watir 程序在运行时，允许测试人员在该测试机器上访问其他网页或者进行其他操作而不会影响到对象识别的结果。

### Example

```
require 'watir'

browser = Watir::Browser.new
browser.goto 'google.com'
browser.text_field(title: 'Search').set 'Hello World!'
browser.button(type: 'submit').click

puts browser.title
# => 'Hello World! - Google Search'
browser.close
```

