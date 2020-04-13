# interview_Q&A

## \#Q



### **iOS**

#### swift

1. 为什么 Apple 建议使用 `Struct`？有何特性？与 `Class` 对比好处在哪里？平常使用多么？ 为什么？★★★☆☆ 
2. 高阶函数`map`、 `flatmap`、 `reduce`、 `filter`作用  `(进阶：自己实现map函数应该如何实现)`★★☆☆☆ 
3. `String` 和 `NSString` 的区别和联系★★☆☆☆ 
4. `associatedType` 的作用★★☆☆☆ 
5. `open`和`public`的区别★★☆☆☆ 
6. 闭包与函数的区别★★☆☆☆ 
7. [`optional`原理与实现机制](#optional原理与实现机制) ★★☆☆☆ 
8. 定义静态方法时关键字`static`和`class`有什么区别? ★☆☆☆☆ 
9. `Swift`中的`Error`与`OC`的`NSError`相互转化时发生了什么? 
10. `Swift method dispatch` ★★★☆☆ 

#### 基础

1. `weak` 和 `assign` ★★☆☆☆
2. `weak`修饰的属性自动值为`nil`的原理★★★☆☆
3. 什么时候使用`copy`修饰符? ★★☆☆☆
4. 邮`roperty(copy, nonautomic) NSMutableArray *array`;会出现什么问题? ★★☆☆☆ 
5. 介绍一下对深拷贝和浅拷贝的理解★★★☆☆ 
6. `ARC`和 `MRC`的 区 别 ★★★☆☆ 
7. `ARC`和 `GC`的 区 別 ★★★☆☆
  - 平时怎么使用 `AutoreleasePool`? ★★★☆☆
  - 不手动指定`AutoreleasePool`的前提下，一个`AutoreleasePool`对象在什么时刻释放? (比如在一个VC的`viewDidLoad`中创建的局部变里) ★ ★ ★ ☆ ☆ 
8. `AutoreleasePool` 和 `RunLoop` 有什么关系? ★★★★☆
9. 介绍一下对`RunLoop`的认识★★★☆☆
10. `RunLoop`和线程有什么关系? ★★★☆☆
11. 猜想一下`RunLoop`内部是如何实现的? ★★★★☆
    0C中self和super有什么关系? ★★★☆☆ 
12. 为什么`block`可以修改使用_block修饰的局部变里昵?(延伸问题:为什么苹果没有设计成默认加上_block )★★★★☆ 
13. `NSTimer`循环引用`self`的问题怎么解决?
 14. 使用`GCD`或`UlView.animate`相关的`api`时，是否考虑引用循环问题? ★★★☆☆
   - `GCD`的队列分为哪两种?
   - `dispatch_barrier_async` 有什么作用? ★★★☆☆
   - `Objective-C`的消息处理流程★★★★☆
   - 介绍一下`iOS ResponseChain` (事件响应链)★★★★☆ 

#### 应用

1. 如何手动触发一个`value`的`KVO`? ★★★☆☆ 

2. `KVC`和`KVO`的`keyPath` —定是属性么? ★★★☆☆ 

3. `IBOutlet`连出来的视图属性为什么可以被设置成`weak` ?★★☆☆☆ 

4. `layoutSubviews` 调用时机★★★☆☆ 

5. `drawRect` 调用时机★★★☆☆

6. `lldb(gdb)`常用的调试命令? ★★★☆☆ 

7. 对比一下`GPU`和`CPU`绘制情况★★★☆☆ 

8. `CGxxx`类的方法使用`GPU`还是`CPU`绘制? ★★★☆☆ 

9. 介绍一下对`离屏渲染`的理解★★★★☆ 

10. 只要屏幕上有任何手势操作都需要执行一个单例对象的方法，如何做？★★★☆☆ 

11. 若要加载多张图片，然后合并成一张整图，用`GCD`怎么做? ★★★☆☆ 

12. 如何让 `NSMutableArray`线程安全? ★★★☆☆ 

    

### 前端

#### 基础

#### Vue



### 算法&数据结构

1. 创建一个链表并翻转★★★☆☆ 

2. 介绍一下常见的几个排序算法的优缺点★★★☆☆ 

3. 扑克牌问题★★★☆☆ 

4. 二叉树是否相等★★★☆☆ 

5. 使用两个队列模拟栈如何做★★★☆☆ 

   

### 网络相关知识

1. `HTTP` 的结构★★☆☆☆

2. `HTTP`和`HTTPS`的区别★★☆☆☆

3. 为 什么 `HTTPS`更安全? ★★☆☆☆

4. `HTTP2` 了解么? ★★☆☆☆ 

5. 在浏览器地址栏里输入一个`URL`到显示出页面，中间都发生了什么? ★★★★☆

   

### 设计模式

1. **`MVC`、`MVVM`、`VIPER`** 优缺点★★★☆☆ 

2. 工程组件化方案★★★★☆ 

3. 简单工厂和抽象工厂的区别

4. [抽象类与接口的区别](#抽象类与接口的区别)

   

### 项目经验(主要根据项目情况问问题)

- 项目中遇到的技术难点有哪些，怎么解决的? 
- 数据持久化方案★★★★☆
-  `APP`启动优化主要做了哪些努力★★★☆☆ 



## \#*Q&A*



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