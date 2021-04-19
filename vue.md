<!--
 * @Author: your name
 * @Date: 2021-02-23 11:03:09
 * @LastEditTime: 2021-04-19 10:12:16
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/vue.md
-->
#### 1.vue dom异步更新机制

#### 2.computed和watch的区别
+ computed是计算一个新的属性，并将新属性挂载到Vue实例上；而watch是监听已经挂载到Vue实例上的属性
+ computed适用一个数据被多个数据影响，而watch适用一个数据影响多个数据
+ computed不支持异步，具有缓存性，而watch不支持异步也不支持缓存

#### 3.Vue的双向数据绑定原理 数据监听，为什么要舍弃Object.defineProperty(),改成用Proxy
主要通过数据劫持+发布订阅者模式实现的。
数据劫持是通过Object.defineProperty()实现，在Vue3.0中改成用Proxy实行。

#### 4.列表中的key值的作用
就地复用 diff算法
https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/1


#### 5.vue路由实现原理
vue路由有两种模式：hash模式、history模式
+ hash模式：通过监听window.hashchange事件（地址栏中hash变化触发）驱动页面变化
+ history模式：通过HTML5的History API来操作的，监听window.popstate事件（浏览器的前进或后退点击触发）驱动页面变化；
+ abstract模式：所有JS环境下均可以，Node环境下会自动强制进入此模式


#### 6. vue组件的根结点在2.0为什么只能有一个, 3.0可以有多个根结点


#### 7.虚拟DOM是如何更新的