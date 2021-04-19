<!--
 * @Author: your name
 * @Date: 2021-02-21 15:58:59
 * @LastEditTime: 2021-04-19 10:20:48
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/http.md
-->
### 1.Http请求方法（动词）
+ GET：获取资源
+ POST：创建资源
+ PUT：更新资源（客户端提供改变后的完整资源）
+ PATCH：更新资源（更新部分属性）
+ DELETE：删除资源
+ HEAD：同GET，但是不会返回资源的主体内容
+ OPTIONS：用于描述目标资源所支持的通信选项（通常在跨域请求时候，会先发起一个预请求）
+ CONNECT：用于建立隧道
+ TRACE：执行一个消息环回测试

### 2.Http请求1.0、1.1、2.0之间的区别
http/1.0 使用的是非持续连接  
http/1.1 使用的是持续连接（对于同一个域，大多数浏览器支持同时建立6个持久连接）缺点：队头堵塞  
http/2 二进制协议、多路复用、数据流、头信息压缩、服务器推送（主动推送静态资源）  

### 3.Http的状态码
+ 1XX：服务器收到请求
+ 2XX：请求成功
+ 3XX：重定向
+ 4XX：客户端错误
+ 5XX：服务端错误

常见的有：200—请求成功，301—永久重定向，302—暂时重定向，304—请求的资源未修改，404—请求的资源不存在，405—请求的方法被禁止

### 4.谈谈对RESTFul的理解

### 5.Http缓存策略
+ 缓存位置
  1、 Service Worker（传输协议必须是Https）
  自由控制缓存条件，如果没有命中缓存，再根据缓存查找优先级去查找缓存，浏览器最终显示是从Service Worker中获取数据.

  2、 Memory Cache(内存)
  内存缓存读取高效，但是持续时间短。进程结束就会释放内存，tab页关闭缓存就会释放.
  访问页面之后再次刷新页面，很多资源都是from Memory Cache.
  preloader指令(如`<link rel="prefetch"/>`)下载的资源是缓存在内存中.

  3、 Disk Cache(硬盘)
  硬盘缓存的优点是容量大，虽然读取速度比内存读取慢，大部分的资源都被缓存在硬盘中。

  4、 Push Cache(Http/2中)

- 缓存策略
强缓存：
expires —— Http/1.0的产物，指定缓存过期时间，受限于客户端时间，不可靠  
Cache-Control：  
协商缓存：  

[详情查看](https://blog.csdn.net/csdnnews/article/details/89324384)

### 6.跨域问题

