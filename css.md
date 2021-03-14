<!--
 * @Author: your name
 * @Date: 2021-03-11 00:08:32
 * @LastEditTime: 2021-03-14 10:37:23
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /Front-End-Notebook/css.md
-->
#### 1.BFC
```
  BFC => Block Format Context
  块级格式上下文，是一个独立的布局环境。里面的元素和外面的元素互相不干扰
  
  创建方式如下：
  + html根元素
  + float浮动
  + 绝对定位
  + overflow不为visible
  + display为表格布局或弹性布局

  作用如下：
  + 清除浮动，避免高度塌陷。计算BFC的高度时，浮动元素也参与计算
  + 避免margin重叠，同一个BFC的相邻元素margin会重叠，不同BFC不会重叠

```

#### 2.居中