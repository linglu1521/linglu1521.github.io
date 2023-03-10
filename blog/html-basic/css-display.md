# CSS 显示模式

## 块级元素

显示特点：

1. 独占一行（一行只能显示一个）
2. 宽度默认是父元素的100%，高度默认由内容撑开
3. 可以设置宽度和高度

代表标签：

```html
div p h系列 ul li dl dt dd from header nav fotter
```







## 行内元素

显示特点：

1. 一行可以显示多个
2. 宽度和高度默认由内容撑开
3. 不可以设置宽高

代表标签：

```html
a span b u i s strong ins em del
```





## 行内块元素

显示特点：

1. 一行可以显示多个
2. 可以设置宽高

代表标签：

```html
input textarea button select
```

- 特殊情况：img标签有行内块元素特点，但是Chrome调试工具中显示结果是inline



## 元素显示模式转换

```css
display: block;
```

目的：改变元素默认的显示特点，让元素复合布局要求

语法：

| 属性                  | 效果             | 使用频率 |
| --------------------- | ---------------- | -------- |
| display: block        | 转换为块级元素   | 较多     |
| display: inline-block | 转换为行内块元素 | 较多     |
| display: inline       | 转换为行内元素   | 极少     |



## HTML 嵌套规范注意点

- 块级元素一般作为大容器
- 可以嵌套文本，块级元素，行内元素，行内块元素

> p 标签中不要嵌套 div p h 等块级元素

- a 标签内部可以嵌套任意内容

> a 标签不能嵌套 a 标签

