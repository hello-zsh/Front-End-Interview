<!--
 * @Author: your name
 * @Date: 2021-02-23 11:03:09
 * @LastEditTime: 2021-03-14 22:02:43
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/vue.md
-->
#### 1.vue dom异步更新机制

#### 2.computed和watch的区别
```
  + computed是计算一个新的属性，并将新属性挂载到Vue实例上；而watch是监听已经挂载到Vue实例上的属性
  + computed适用一个数据被多个数据影响，而watch适用一个数据影响多个数据
  + computed不支持异步，具有缓存性，而watch不支持异步也不支持缓存
```

#### 3.Vue的双向数据绑定原理 数据监听，为什么要舍弃Object.defineProperty(),改成用Proxy
```
  主要通过数据劫持+发布订阅者模式实现的。
  数据劫持是通过Object.defineProperty()实现，在Vue3.0中改成用Proxy实行。
  
```

#### 4.列表中的key值的作用
就地复用 diff算法
https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/1

