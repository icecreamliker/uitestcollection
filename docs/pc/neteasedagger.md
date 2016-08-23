# NetEase/Dagger

> github： https://github.com/NetEase/Dagger  

> Star: 282  
> Fork: 170  
> Watch: 75    
> Up to 2016.08.17  

### 概述

Dagger是网易杭州研究院QA团队开发的一个轻量级、运行稳定的WebUI自动化测试框架，主要基于Selenium及TestNG可以认为是对Selenium进行二次封装的一个框架（俗称 造轮子 ）。之所以把这个轮子开源出来，主要在于经过了公司内部多个项目的实践，也取得了不错的成效，因此，希望开源以后可以对大家有所帮助及参考。

### 主要特性

API极少，易于上手  
支持单机多浏览器并发执行，大大缩短用例执行时间  
通过修改TestNG源码实现失败用例自动重运行,由此几乎消除WebUI自动化中常见的虚假失败
默认使用Chrome浏览器  
失败用例自动截屏  
支持数据驱动测试  
图片对比功能，主要通过抓取页面控件和截图的方式，在图片的像素级别上对比不同版本的截图来进行页面样式的检查  

### 如何使用

Dagger十分适合中小型团队从零开始WebUI自动化，这样的话，如果要下载整个Dagger代码，需要在本地配置好maven环境(Eclipse需要配置maven插件)，用maven构建测试用例，下载后看一下使用文档就可以直接开始写用例了

也可以把Dagger打成Jar包，导入已有的自动化框架中，或者直接下载 dagger-1.2.jar

现阶段我们使用selenium-server-standalone-2.37.0.jar 和 selenium-safari-driver-2.37.0.jar，相关配置可以在pom.xml中进行修改

另外，如果有需要可以下载chromedriver_for_win_2.3.exe 和 iedriver_win32_2.37.0.exe，建议将.exe 文件都放在 res 文件夹下

配置文件prop.properties和imagecheck.properties需要在工程下另外创建，其中imagecheck.properties用于配置图片对比检查样式的相关参数