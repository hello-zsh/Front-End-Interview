<!--
 * @Author: your name
 * @Date: 2021-02-23 23:33:02
 * @LastEditTime: 2021-04-19 10:14:15
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/js.md
-->
#### 1.null和undefined的区别
Undefined和Null都是ES里面的基本数据类型，它们都只有一个值分别是undefined和null。
+ undefined: 声明了一个变量，但是未对它进行初始化，这个变量的值就是undefined。
+ null: 空对象指针，指示变量未指向任何对象。将变量值设为null,可以解除引用。

#### 2.原型、原型链
相关方法：
1. isPrototypeOf() 
  查找一个对象是否在另一个对象的原型链上
  Person.prototype.isPrototypeOf(student)
2. Object.getPrototypeOf()
  Object.getPrototypeOf(student) === Person.prototype
3. for-in
  遍历实例以及原型上的可选属性
4. Object.keys()
  遍历实例上可选属性
5. Object.getOwnPrototypeNames()
  遍历实例上所有属性（包括不可枚举属性）

#### 3.call和apply的区别
相同点：都可以改变函数上下文对象,即this的指向，第一个参数，为null或undefined指定为全局对象
不同点：
  call() 接受的是参数列表，如call(null, 1, 2, 3) 
  apply() 接受的是参数数组，如apply(null, [1, 2, 3])

bind() 返回的是改变了函数上下文对象的一个新函数，第一个参数是函数上下文对象，后面的参数列表将作为新函数的参数

#### 4.防抖和节流
具体实现方式参考lodash

#### 5.fetch和HTTP的区别

#### 6.判断变量类型的几种方式
+ `typeof`
  typeof无法识别null、数组，都会识别成object

+ `instanceof`
  instanceof是判断一个对象是否是另一个对象的实例(object instanceof constructor)，只有通过构造函数创建的才能检测出来,如下：
```
  const test1 = new Array(5);
  test1 instanceof Array; //true
  test1 instanceof Object; //true
```

+ `Object.prototype.toString.call()`
返回类似`[object Number]`这样的字符串

#### 7.堆和栈的区别

#### 8.闭包
闭包：引用了另一个函数作用域中变量的函数，通常是在嵌套函数中实现的。
作用： 可以读取函数内部的变量

#### 9.实现深度拷贝


#### 10.script标签的defer、async属性
+ 什么都不加，浏览器读到就会立即加载并执行相应的脚本，会阻塞后续文档的加载
+ async，异步加载脚本，加载完成之后立刻执行脚本，一般用于第三方脚本
+ defer，异步加载脚本，并且在页面完成解析时执行脚本

#### 11.事件循环机制



