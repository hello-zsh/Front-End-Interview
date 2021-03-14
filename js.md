<!--
 * @Author: your name
 * @Date: 2021-02-23 23:33:02
 * @LastEditTime: 2021-03-14 19:18:18
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/js.md
-->
#### 1.null和undefined的区别
```
  Undefined和Null都是ES里面的基本数据类型，它们都只有一个值分别是undefined和null。
  undefined: 声明了一个变量，但是未对它进行初始化，这个变量的值就是undefined。
  null: 空对象指针，指示变量未指向任何对象。将变量值设为null,可以解除引用。
```

#### 2.原型、原型链
```
  相关方法：
  1、isPrototypeOf() 
    查找一个对象是否在另一个对象的原型链上
    Person.prototype.isPrototypeOf(student)
  2、Object.getPrototypeOf()
    Object.getPrototypeOf(student) === Person.prototype
  3、for-in
    遍历实例以及原型上的可选属性
  4、Object.keys()
    遍历实例上可选属性
  5、Object.getOwnPrototypeNames()
    遍历实例上所有属性（包括不可枚举属性）
```

#### 3.call和apply的区别
```
  相同点：都可以改变函数上下文对象,即this的指向，第一个参数，为null或undefined指定为全局对象
  不同点：
    call() 接受的是参数列表，如call(null, 1, 2, 3) 
    apply() 接受的是参数数组，如apply(null, [1, 2, 3])

  bind() 返回的是改变了函数上下文对象的一个新函数，第一个参数是函数上下文对象，后面的参数列表将作为新函数的参数
```

#### 4.防抖和节流
具体实现方式参考lodash

#### 5.fetch和HTTP的区别

#### 6.typeof、instanceof的区别
```
  typeof判断一个变量是什么类型
  typeof无法识别null、数组，都会识别成object

  instanceof是判断一个对象是否是另一个对象的实例(object instanceof constructor)
  
  const test1 = new Array(5);
  test1 instanceof Array; //true
  test1 instanceof Object; //true

```
