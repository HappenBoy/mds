## Kotlin协程

#### 什么是协程？

###### 讲什么是协程之前，首先大家要知道什么是进程和线程？以及进程、线程和协程之间的区别与联系？

1. 进程

2. 线程

3. 进程和线程之间的区别与联系

4. 协程定义

   协程是上层编程语言的能力，不需要操作系统和硬件支持，是编程语言为了让开发者更容易写出协作式任务的代码，而封装的一种任务调度能力

5. 协程特点

   - 协程是上层编程语言的能力，不需要操作系统和硬件的支持
   - 协程实现依赖于线程，不能脱离线程而存在
   - 协程由程序自己调度
   - 协程通过程序调度可以执行在一个或多个线程之中
   - 协程让程序更易读（异步逻辑同步写）

#### Kotlin协程的基础设施

1. 协程创建
   - 不带接收者
   - 
   - 带接收者
2. 协程启动



#### CoroutineContext

特点：

1. 既有Map的特点，也有Set的特点
2. 每个元素都是Element，每个Element都有一个Key与之对应，相同的Key的Element不可以同时存在，Element之间可以通过**+**号组合起来。

组成：

主要由对下四个元素组成

1. Job

   协程的唯一标识，用来控制协程的生命周期（new\active\completing\completed\cancelling\cancelled）

2. CoroutineDispatcher

   指定协程运行的线程（IO\Default\Main\Unconfined）

3. CoroutineName

   指定协程的名称，默认为coroutine

4. CoroutineExceptionHandler

   指定协程的异常处理器，用来处理未捕获的异常

#### RestrictsSuspension注解

1.  此注解用于修饰类或接口

2. 修饰的类做为挂起函数接收者类型时，协程体内部只能调用此类内部声明的挂起函数，不能调用其它挂起函数

   ```kotlin
   
   ```

   