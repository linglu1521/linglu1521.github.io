# CSS 层叠样式表

Cascading style sheets

## 语法规则

```txt
选择器 {
	属性名: 属性值
}
```

## 书写位置

```html
<head>
    <title></title>
    <style>
    	/* 这里写css */
    </style>
</head>
```

## CSS 引入方式

| 引入方式 | 书写位置                | 作用范围 | 使用场景   |
| :------- | ----------------------- | -------- | :--------- |
| 内嵌式   | style标签               | 当前页面 | 小案例     |
| 外链式   | link标签引入单独css文件 | 多个页面 | 项目中     |
| 行内式   | 标签style属性中         | 当前标签 | 配合js使用 |

（1）内嵌式

- CSS 写在style标签中
- style标签可以写在页面任意位置，一般放在head标签中


[](demo/css-1.html ':include :type=code')

[](demo/css-1.html ':include height=165')

（2）外链式

- CSS 写在单独的`.css`文件中
- 通过 link 标签引入到网页中

[](demo/css-2.css ':include :type=code')

[](demo/css-2.html ':include :type=code')

[](demo/css-2.html ':include height=60')

（3）行内式

- CSS写在标签style属性中

```html
<div style="color: green"; background-color: #f1f1f1>
    这是一段设置了css样式的文字
</div>
```


<output>

<div style="color: green"; background-color: #f1f1f1>
    这是一段设置了css样式的文字
</div>

</output>