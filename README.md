- [iOS](#ios)
    - [Swift](#swift)
    - [基础](#基础)
    - [应用](#应用)
- [前端](#前端)
    - [基础](#基础-1)
    - [Vue](#vue)
- [算法&数据结构](#算法数据结构)
- [网络相关知识](#网络相关知识)
- [设计模式 & 架构](#设计模式-架构)
- [项目经验(主要根据项目情况问问题)](#项目经验主要根据项目情况问问题)
- [\#Q&A](#qa)
    - [抽象类与接口的区别](#抽象类与接口的区别)
    - [optional原理与实现机制](#optional原理与实现机制)
    - [方法交换（swizzle）应该放在哪里执行](#方法交换swizzle应该放在哪里执行)
    - [KVC和KVO的keyPath—定是属性么](#kvc和kvo的keypath定是属性么)
    - [App优化](#app优化)
    - [关于swift与OC多说两句](#关于swift与oc多说两句)
    - [HTTP的三次握手和四次挥手以及为什么挥手是四次](#http的三次握手和四次挥手以及为什么挥手是四次)
    - [悬垂指针、野指针分别指什么](#悬垂指针-野指针分别指什么)
    - [float与double](#float与double)

## iOS

#### Swift

1. 为什么 Apple 建议使用 `Struct`？有何特性？与 `Class` 对比好处在哪里？平常使用多么？ 为什么？★★★☆☆ 
2. 高阶函数`map`、 `flatmap`、 `reduce`、 `filter`作用  `(进阶：自己实现map函数应该如何实现)`★★☆☆☆ 
3. `String` 和 `NSString` 的区别和联系★★☆☆☆ 
4. `associatedType` 的作用？简述其与泛型的区别★★☆☆☆ 
5. `open`和`public`的区别★★☆☆☆ 
6. 闭包与函数的区别★★☆☆☆ 
7. [`optional`原理与实现机制](#optional原理与实现机制) ★★☆☆☆ 
8. 定义静态方法时关键字`static`和`class`有什么区别? ★☆☆☆☆ 
9. `Swift`中的`Error`与`OC`的`NSError`相互转化时发生了什么? ★★★☆☆ 
10. `Swift method dispatch` ★★★☆☆ 
11. [swift 单例的实现，是如何保证线程安全的](https://juejin.im/post/59e30701f265da432f3026ad)★★☆☆☆ 
12. [关于swift与OC多说两句](#关于swift与OC多说两句)

#### 基础

1. `weak` 和 `assign` ★★☆☆☆
2. [悬垂指针、野指针分别指什么？](#悬垂指针、野指针分别指什么)
3. `weak`原理和实现★★★☆☆
4. 什么时候使用`copy`修饰符? ★★☆☆☆
5. 邮`roperty(copy, nonautomic) NSMutableArray *array`;会出现什么问题? ★★☆☆☆ 
6. 介绍一下对深拷贝和浅拷贝的理解★★★☆☆ 
7. `ARC`和 `MRC`的 区 别 ★★★☆☆ 
8. `ARC`和 `GC`的 区 別 ★★★☆☆
  - 平时怎么使用 `AutoreleasePool`? ★★★☆☆
  - 不手动指定`AutoreleasePool`的前提下，一个`AutoreleasePool`对象在什么时刻释放? (比如在一个VC的`viewDidLoad`中创建的局部变里) ★ ★ ★ ☆ ☆ 
9. `AutoreleasePool` 和 `RunLoop` 有什么关系? ★★★★☆
10. 介绍一下对`RunLoop`的认识和几种Timer★★★☆☆
11. `RunLoop`和线程有什么关系? ★★★☆☆
12. 猜想一下`RunLoop`内部是如何实现的? ★★★★☆
    0C中self和super有什么关系? ★★★☆☆ 
13. 为什么`block`可以修改使用_block修饰的局部变里昵?(延伸问题:为什么苹果没有设计成默认加上_block )★★★★☆ 
14. `NSTimer`循环引用`self`的问题怎么解决?★★☆☆☆ 
 15. 使用`GCD`或`UlView.animate`相关的`api`时，是否考虑引用循环问题? ★★★☆☆
   - `GCD`的队列分为哪两种?
   - `dispatch_barrier_async` 有什么作用? ★★★☆☆
   - `Objective-C`的消息处理流程★★★★☆
   - 介绍一下`iOS ResponseChain` (事件响应链)★★★★☆ 
16. [`float`与`double`有效位，为什么](#float与double)★★★★★

#### 应用

1. 如何手动触发一个`value`的`KVO`? ★★★☆☆ 

2. [`KVC`和`KVO`的`keyPath` —定是属性么?](#KVC和KVO的keyPath—定是属性么) ★★★☆☆ 

3. OC语言如何是管理内存? 如何检测内存泄漏? 有几种方式？

4. `IBOutlet`连出来的视图属性为什么可以被设置成`weak` ?★★☆☆☆ 

5. `layoutSubviews` 调用时机★★★☆☆ 

6. `drawRect` 调用时机★★★☆☆

7. `lldb(gdb)`常用的调试命令? ★★★☆☆ 

8. 对比一下`GPU`和`CPU`绘制情况★★★☆☆ 

9. `CGxxx`类的方法使用`GPU`还是`CPU`绘制? ★★★☆☆ 

10. 介绍一下对`离屏渲染`的理解★★★★☆ 

11. 只要屏幕上有任何手势操作都需要执行一个单例对象的方法，如何做？★★★☆☆ 

12. 若要加载多张图片，然后合并成一张整图，用`GCD`怎么做? ★★★☆☆ 

13. 如何让 `NSMutableArray`线程安全? ★★★☆☆ 

14. [方法交换（swizzle）应该放在哪里执行？为什么？](#方法交换（swizzle）应该放在哪里执行)★★☆☆☆

15. 简述一下 OC 和 JS 相互调用的几种方式？[这里](https://juejin.im/post/5a95272f5188257a585113a3) [还有这里]([https://xiaovv.me/2017/04/15/iOS%E4%B8%8BJS%E4%B8%8ESwift%E4%BA%92%E7%9B%B8%E8%B0%83%E7%94%A8%EF%BC%88%E5%9B%9B%EF%BC%89JavaScriptCore/](https://xiaovv.me/2017/04/15/iOS下JS与Swift互相调用（四）JavaScriptCore/))★★★★☆

16. [如何设计一个图片缓存框架？](https://www.jianshu.com/p/419681149cdf)★★★★☆

   ​    

## 前端

#### 基础

#### Vue



## 算法&数据结构

1. 创建一个链表并翻转★★★☆☆ 

2. 如何判断链表是否有环★★★☆☆ 

3. 介绍一下常见的几个排序算法的优缺点★★★☆☆ 

4. 扑克牌问题★★★☆☆ 

5. 二叉树是否相等★★★☆☆ 

6. 使用两个队列模拟栈如何做★★★☆☆ 

7. 快速排序是否稳定? 能否手写快排★★★★☆

    

## 网络相关知识

1. `HTTP` 的结构★★☆☆☆

2. `HTTP`和`HTTPS`的区别★★☆☆☆

3. 为 什么 `HTTPS`更安全?简述HTTPS握手过程与加密★★☆☆☆

4. Websocket 和 sockect 的区别[[简述](https://juejin.im/post/5c974855e51d4572f05e110a)]★★★★☆

5. `HTTP2` 了解么? ★★☆☆☆ 

6. 什么是中间人攻击？★★★☆☆

7. Dns 解析的风险 劫持跟踪和欺诈★★★★☆

8. [HTTP的三次握手和四次挥手以及为什么挥手是四次？](#HTTP的三次握手和四次挥手以及为什么挥手是四次)★★★☆☆

9. 在浏览器地址栏里输入一个`URL`到显示出页面，中间都发生了什么? ★★★★☆

    

## 设计模式 & 架构

1. **`MVC`、`MVVM`、`VIPER`** 优缺点★★★☆☆ 

2. 工程组件化方案★★★★☆ 

3. 简单工厂和抽象工厂的区别★★★☆☆ 

4. [抽象类与接口的区别](#抽象类与接口的区别)★★★☆☆ 

5. app模块化与路由（模块间通信）★★★★☆

    

## 项目经验(主要根据项目情况问问题)

- 项目中遇到的技术难点有哪些，怎么解决的? 
- 数据持久化方案★★★★☆
-  [`App`优化（启动优化和性能优化）](#App优化)★★★☆☆ 



## \#Q&A



> 说明：解答部分为个人理解加工，非标准答案



#### 抽象类与接口的区别

​	抽象类是对`具体事物`的抽象，接口是对一类`属性`/`动作`的抽象。

​	当确定有一类事物，但不知具体有什么实例化（例如Object、vehicle），用抽象类；当描述一类特性的时候，用接口（例如 Movable， Flyable）



#### optional原理与实现机制

​	optional底层实现为枚举，模拟实现：

```swift
enum Optional<T> {    
  case some(T)   //对于所有成功的情况，我们用case some，并且把成功的结果保存在associated value里；
  case none      //对于所有错误的情况，我们用case none来表示；
}
```

#### 方法交换（swizzle）应该放在哪里执行

​	方法交换应保证在程序运行期间只执行一次，从这个角度来讲，将其放在单例，或者类的load()方法中皆可。

#### KVC和KVO的keyPath—定是属性么

不一定，OC中成员变量也是可以的。
处注意属性与成员变量的区别，OC中使用@property时，实际声明的为一个计算属性，编译器会为属性生成setter()与getter(), 并会为该属性添加@sythesize生成带下划线的对应存储属性（即成员变量），典型的能说明这个问题的场景是：如果同时重写了setter与getter 必须提供一个自己实现的成员变量，否则会报错。
此题容易扩展sythesize关键字作用，及如何手动触发KVO

[深入理解](https://juejin.im/entry/5bea93345188256d014d5fa9)

#### App优化

> **App启动流程：** 
>
> 1. 加载info.plist
> 2. 创建沙盒
> 3. 权限检查
> 4. 库链接
>
> **App初始化流程**:
>
> 1. `main` 函数
>
> 2. 执行`UIApplicationMain`      
>
> 3. 1. 创建`UIApplication`对象
>    2. 创建`UIApplication`的`delegate`对象
>    3. 创建`MainRunloop`
>    4.  `delegate`对象开始处理(监听)系统事件(没有`storyboard`)
>
> 4. 根据`Info.plist`获得最主要`storyboard`的文件名,加载最主要的`storyboard`(有`storyboard`)
>
> 5. 程序启动完毕的时候,  就会调用代理的`application:didFinishLaunchingWithOptions:`方法在`application:didFinishLaunchingWithOptions:`中创建`UIWindow` 创建和设置`UIWindow`的rootViewController
>
> 6. 最终显示第一个窗口

#### 关于swift与OC多说两句

OC真的太老了，作为一个从上个世纪修修补补流传下来的语言，从命名都感觉出是仓促上马的项目。没有C的效率，没有Java的灵活，没有C++的类型安全，甚至对于泛型的支持都乏善可陈。使用OC的过程中，从头到尾都有一种“这种特性比较牛逼，但是我们实现不了，来加个库打个补丁吧”的割裂感，一面为了让语言的功能更强大给语言添加上动态性runtime，一面又不支持开发者对于runtime的过度使用，连函数派发的方式都匪夷所思。不过还好Apple趁着还身强体壮又要了一个Swift，所以我面试的时候一定会问“贵公司的项目是用跟shit一样的OC写的吗？”QAQ

#### HTTP的三次握手和四次挥手以及为什么挥手是四次

之所以握手三次，是因为在第二次握手中，服务器同时将syn与ack发送给客户端，即将两次握手过程在一次完成

#### 悬垂指针、野指针分别指什么

基本属于语义的区别：

- **悬垂指针**：当所指向的对象被释放或者收回，但是对该指针没有作任何的修改，以至于该指针仍旧指向已经回收的内存地址，此情况下该指针便称**悬垂指针**（也叫**迷途指针**）。

- **野指针：**某些编程语言允许**未初始化**的指针的存在，而这类指针即为**野指针**。

#### float与double

- 单精度浮点数 `float` 总共包含 32 位，其中 1 位表示符号、8 位表示指数，最后 23 位表示小数；

- 双精度浮点数 `double` 总共包含 64 位，其中 1 位表示符号，11 位表示指数，最后 52 位表示小数；

  [详细说明](https://mp.weixin.qq.com/s/M2m3haos2OebXyXFzTc_6A)