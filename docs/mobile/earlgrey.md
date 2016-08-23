#google/EarlGrey 

> github： https://github.com/google/EarlGrey

> Star: 2922    
> Fork: 331         
> Watch: 195      
> Up to 2016.08.17  
> 

### What is EarlGrey?
EarlGrey is a native iOS UI automation test framework that enables you to write clear, concise tests.

With the EarlGrey framework, you have access to enhanced synchronization features. EarlGrey automatically synchronizes with the UI, network requests, and various queues; but still allows you to manually implement customized timings, if needed.

EarlGrey’s synchronization features help to ensure that the UI is in a steady state before actions are performed. This greatly increases test stability and makes tests highly repeatable.

EarlGrey works in conjunction with the XCTest framework and integrates with Xcode’s Test Navigator so you can run tests directly from Xcode or the command line (using xcodebuild).

### EarlGrey所提供的主要特性如下所示，这些特性使得应用的测试变得更加轻松，也更具效率：

* 强大的内建同步机制：测试会在与UI进行交互前自动等待动画、网络请求等事件。这样，我们就可以更加轻松地编写测试了（无需睡眠，也不必再等待了），同时维护起来也更加容易（非常直观，整个测试看起来就是一系列描述而已）。一般来说，你无需考虑同步性，因为EarlGrey会自动同步UI、网络请求、主Dispatch Queue以及主NSOperationQueue。为了支持在下一个UI交互发生前需要等待某个事件出现这种场景，EarlGrey提供了Synchronization APIs，你可以通过他们来控制EarlGrey的同步行为。你可以使用这些APIs来增强测试的稳定性。   

* 可见性检测：所有的交互都发生在用户可以看到的元素上。比如说，尝试轻拍图片后面的按钮会导致测试立刻失败。EarlGrey使用了屏幕截图区分比较（也叫做“screenshot diffs”）在与UI元素交互前确定其可见性。这样，你就可以确定对于EarlGrey与之交互的UI，用户可以看到并且也能与之交互。值得注意的是，进程外（即系统生成的）警告视图与其他会遮盖住UI的模态对话框会对这个过程产生干扰。    

* 灵活的设计：用于确定元素选择、交互、断言与同步的组件在设计上就是可扩展的。轻拍与滑动是通过应用级的触摸事件来实现的，而不是使用元素级的事件处理器。在每一次UI交互前，EarlGrey都会断言交互的元素是可见的，而不仅仅是存在于视图层次体系中就行了。EarlGrey的UI交互模拟了真实用户与应用UI交互的方式，可以帮助你找到并修复用户在使用应用时所遇到的同样的Bug。

