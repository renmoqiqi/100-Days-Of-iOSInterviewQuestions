
# Runloop 是什么

* Runloop 是一个可以处理，例如window屏幕的键盘触摸事件，以及NSport对象，NSConnection对象，甚至可以处理 NSTimer事件等多个输入源的机制。

* 每个线程都有自己的Runloop，你可以通过currentRunLoop方法获取。

* 通常情况你不需要直接访问Runloop，当需要的时候线程会自动创建。

* 线程的Runloop一没有工作做的时候处于休眠状态，直到有上述几种可以处理的工作。

**注意：NSRunLoop 并不是线程安全的，只能在当前线程的上下文调用他的方法，所以不要尝试在不同的线程调用他的方法，这样会得到你意想不到的结果。**
