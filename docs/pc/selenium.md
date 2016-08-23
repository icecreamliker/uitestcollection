# SeleniumHQ/selenium
> github： https://github.com/SeleniumHQ/selenium

> Star: 4120  
> Fork: 2052   
> Watch: 676    
> Up to 2016.08.17  

### What is Selenium?

Selenium 是一组软件工具集,每一个都有不同的方法来支持测试自动化。大多数使用 Selenium 的QA工程师只关注一两个最能满足他们的项目需求的工具上。然而，学习所有的工具你将有更多选择来解决不同类型的测试自动化问题。这一整套工具具备丰富的测试功能，很好的契合了测试各种类型的网站应用的需要。这些操作非常灵活，有多种选择来定位 UI 元素，同时将预期的测试结果和实际的行为进行比较。Selenium 一个最关键的特性是支持在多浏览器平台上进行测试。

### Selenium 工具集  

*Selenium 由多个软件工具组成，每个具备特定的功能。*

#### Selenium 2 (又叫 Selenium Webdriver)

Selenium 2 代表了这个项目未来的方向，也是最新被添加到 Selenium 工具集中的。这个全新的自动化工具提供了很多了不起的特性，包括更内聚和面向对象的 API，并且解决了旧版本限制。

它支持WebDriver API及其底层技术，同时也在WebDriver API底下通过Selenium 1技术为移植测试代码提供极大的灵活性。此外，为了向后兼容，Selenium 2 仍然使用 Selenium 1 的 Selenium RC 接口。

#### Selenium 1 (又叫 Selenium RC 或 Remote Control)

在很长一段时间内，Selenium RC 都是最主要的 Selenium 项目，直到 WebDriver 和 Selenium 合并而产生了最新且最强大的 Selenium 2.

Seleinum 1 仍然被活跃的支持着（更多是维护），并且提供一些 Selenium 2 短时间内可能不会支持的特性，包括对多种语言的支持(Java, Javascript, Ruby, PHP, Python, Perl and C#) 和对大多数浏览器的支持。 

#### Selenium-Grid   

Selenium-Grid 使得 Selenium RC 解决方案能提升针对大型的测试套件或者哪些需要运行在多环境的测试套件的处理能力。Selenium Grid 能让你并行的运行你的测试，也就是说，不同的测试可以同时跑在不同的远程机器上。这样做有两个有事，首先，如果你有一个大型的测试套件，或者一个跑的很慢的测试套件，你可以使用 Selenium Grid 将你的测试套件划分成几份同时在几个不同的机器上运行，这样能显著的提升它的性能。同时，如果你必须在多环境中运行你的测试套件，你可以获得多个远程机器的支持，它们将同时运行你的测试套件。在每种情况下，Selenium Grid 都能通过并行处理显著地缩短你的测试套件的处理时间。

### 支持的浏览器和平台

在 Selenium 2.0 中，支持的浏览器完全取决于你是否使用 Selenium-WebDriver 或 Selenium-RC。

#### Selenium-WebDriver

Selenium-WebDriver 支持如下浏览器，在所有支持这些浏览器的操作系统中能都运行良好。

* Google Chrome 12.0.712.0+
* Internet Explorer 6, 7, 8, 9 - 32 and 64-bit where applicable
* Firefox 3.0, 3.5, 3.6, 4.0, 5.0, 6, 7
* Opera 11.5+
* HtmlUnit 2.9
* Android – 2.3+ for phones and tablets (devices & emulators)
* iOS 3+ for phones (devices & emulators) and 3.2+ for tablets (devices & emulators)    

*注意：*

在写本文档的时候，一款 Android 2.3 的模拟器被报有bug。但是在 tablet 模拟器和真实设备中均工作良好。

Selenium 1.0 and Selenium-RC

这里是指老的，支持 Selenium 1 的部分。它也适用于 Selenium 2 版本中的 Selenium RC。

|Browser|Selenium IDE|Selenium 1 (RC)|Operating Systems|
|---|---|---|---|
|Firefox 3.x|Record and playback tests|Start browser, run tests|Windows, Linux, Mac|
|Firefox 3|Record and playback tests|Start browser, run tests|Windows, Linux, Mac|
|Firefox 2|Record and playback tests|Start browser, run tests|Windows, Linux, Mac|
|IE 8|Test execution only via Selenium RC*|Start browser, run tests|Windows|
|IE 7|Test execution only via Selenium RC*|Start browser, run tests|Windows|
|IE 6  |  Test execution only via Selenium RC*  |  Start browser, run tests |   Windows|
|Safari 4  |  Test execution only via Selenium RC| Start browser, run tests|    Windows, Mac|
|Safari 3  |  Test execution only via Selenium RC |Start browser, run tests|    Windows, Mac|
|Safari 2  |  Test execution only via Selenium RC | Start browser, run tests |   Windows, Mac|
|Opera 10  |  Test execution only via Selenium RC | Start browser, run tests  |  Windows, Linux, Mac|
|Opera 9 |Test execution only via Selenium RC| Start browser, run tests|    Windows, Linux, Mac|
|Opera 8| Test execution only via Selenium RC| Start browser, run tests|    Windows, Linux, Mac|
|Google Chrome |  Test execution only via Selenium RC| Start browser, run tests  |  Windows, Linux, Mac|
|Others | Test execution only via Selenium RC| Partial support possible** | As applicable|