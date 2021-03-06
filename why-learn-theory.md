# 前端学习计算机理论知识的好处
写本文的目的，主要是源于和一个老前端的交流。

我认为学习计算机理论知识很有用，对职业发展帮助非常大。他认为应用开发和底层开发是两回事，前端属于应用开发，学理论知识完全浪费时间。具体细节就不说了，最后是不欢而散。

不过，有一点我们是达成共识的：学习计算机理论知识不能让你的业务页面写得更快、更好，它不是银弹，不能解决所有开发中的问题。如果你还处于入门级别，学这个也没多大用，学好前端基础知识反而更有用（这句话针对非科班出身的前端）。

我认为学习计算机理论知识对于前端来说有两点好处：
1. 知其然，知其所以然
2. 开拓眼界，多维发展

####  1. 知其然，知其所以然
我们都知道，在 JavaScript 中，有两种数据类型，分别为基本类型和引用类型。

**基本类型**
```js
let a, b
a = 1
b = a
b = 3
console.log(a) // 1
console.log(b) // 3
```

**引用类型**
```js
let a, b
a = { msg: 'hello' }
b = a
b.msg = 'world'
console.log(a) // { msg: "world" }
console.log(b) // { msg: "world" }
```
为什么基本类型 b 的值变了，a 不会变？而在引用类型中 b 的值变了，a也跟着变？如果你学习过内存管理以及编译原理相关知识，就可以理解这个现象了。

从程序的角度来看，内存被抽象为一个一维数组，a 和 b 在内存都占着一个位置，并且在内存中存储的是它们各自的值。

而引用类型则不同，在创建一个引用类型数据时，需要在堆中分配一块内存，然后将这块内存的地址返回。即 `a = { msg: 'hello' }` 这个操作，a 存储的是一个地址。执行 `b = a` 后， a 和 b 指向同一个地址。当 `b.msg = 'world'` 这个操作执行时，改变的是这块内存中的值，所以就不难理解为什么在引用类型中 b 的值变了，a 也跟着变了。

以上只是其中一个例子，还有更多例子就不一一列举了。

学习计算机理论知识能让我们不仅仅看到程序的表面，还能看到程序计算的本质。想一想，从你写下一行代码开始，经历词法分析、语法分析、生成机器码，最后变成一条条指令在 CPU 中执行，并且数据在 CPU 与内存之间如何流转你都了然如胸，这种感觉多奇妙。

####  2. 开拓眼界，多维发展
一个好的前端不仅仅是一个前端，不要只盯着眼前的一亩三分地，更要了解前端以外的知识。

一个项目启动前，通常会有一个需求讨论会。如果你不懂理论知识，当聊到数据库、服务器、并发等名词时，你就只能两眼一摸黑，插不上嘴，安安静静的坐在一边。但如果你学过这方面的知识时，你就能和他们一起指点江山，不再是外人。

在前端方向，理论知识也有用武之地。例如 `babel`，就需要用到编译原理；研究 `webgl`，还得用上图形学的知识；学了软件工程，你就明白测试、团队规范的重要性和必要性。说白了，懂计算机理论知识的前端和普通前端是站在不同维度上看问题的。

计算机已经发展几十年了，中间淘汰的技术数不胜数，前端还是最近几年才火起来的，说不定哪天这个职业就没了。如果发生这种情况，你还能干什么？

技术会过时，理论知识不会过时，只要冯诺依曼体系还在，你学的东西就一直有用。学好计算机理论知识，不干前端，还能干别的。

#### 结论
1. 计算机理论知识很有用。
2. 刚入门先学好前端基础知识，感觉水平差不多了，再去学习计算机理论知识。
