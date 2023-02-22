# CSS实战

准备工作

- 在网站项目中需要建立好以下目录：

```
/* 用来存放项目所需要用到的图片 */
imgages文件夹	

/* 用来存放项目所需要用到的css文件，一般与html文件配套。
	eg: index.css */
css文件夹	

/* 网站的首页 */
index.html	
```



清除浏览器默认样式

```css
/* reset.css */

* {
  margin: 0;
  padding: 0;
  /* 内减模式 */
  box-sizing: border-box;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
}

/* 清除浮动 */
.clearfix::before,
.clearfix::after {
  content: '';
  display: table;
}

.clearfix::after {
  clear: both;
}

body {
  background-color: #f3f5f7;
}

/* 版心居中 */
.wrapper {
  width: 1200px;
  margin: 0 auto;
}

```



控制 input placeholder 样式

```css
input::placeholder {
    
}

```



调整图片上下对齐

```css
img {
  vertical-align: middel;
}

```





## 项目：

1. [学成网简单布局]()