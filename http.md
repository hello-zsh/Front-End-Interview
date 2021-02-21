<!--
 * @Author: your name
 * @Date: 2021-02-21 15:58:59
 * @LastEditTime: 2021-02-21 23:04:22
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/http.md
-->
#### 1.Http请求方法（动词）
```
  GET：获取资源
  POST：创建资源
  PUT：更新资源（客户端提供改变后的完整资源）
  PATCH：更新资源（更新部分属性）
  DELETE：删除资源
  HEAD：同GET，但是不会返回资源的主体内容
  OPTIONS：用于描述目标资源所支持的通信选项（通常在跨域请求时候，会先发起一个预请求）
  CONNECT：用于建立隧道
  TRACE：执行一个消息环回测试
```

#### 2.Http请求1.0、1.1、2.0之间的区别

#### 3.Http的状态码
```
  1XX：服务器收到请求
  2XX：请求成功
  3XX：重定向
  4XX：客户端错误
  5XX：服务端错误

  常见的有：200—请求成功，301—永久重定向，302—暂时重定向，304—请求的资源未修改，404—请求的资源不存在，405—请求的方法被禁止
```