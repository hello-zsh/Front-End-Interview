<!--
 * @Author: your name
 * @Date: 2021-03-14 21:55:16
 * @LastEditTime: 2021-04-19 10:22:43
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/webpack.md
-->
#### 1.webpack中的plugin和loader的区别
+ loader: 是一个转换器，将A文件进行编译成B文件，属于单纯的文件转换过程
+ plugin: 是一个扩展器，针对是loader结束之后，webpack整个打包过程，并不直接操作文件，而是基于事件机制工作，会监听webpack打包过程中的某些节点，执行广泛的任务

#### 2.webpack中sourcemap的值有哪些，sourcemap的作用是什么
sourcemap的作用是为了可以定位源代码，解决不好调试代码的问题。  
开发环境推荐使用：eval-cheap-module-source-map  
生产环境推荐使用：cheap-module-source-map  