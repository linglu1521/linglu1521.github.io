# CSS 基础选择器

- 标签选择器
- 类选择器
- id选择器
- 通配符选择器

（1）标签选择器

```txt
标签名 {
	属性名: 属性值;
}
```

```html
<style>
    p {
        color: red;
    }
</style>

<p>hello world</p>
```

<output>

<p style="color: red">hello world</p>

</output>



（2）类选择器

```txt
.类名 {
	属性名: 属性值;
}
```

- 合法的类名：数字，字母，下划线，中划线
- 一个元素可以有多个类名，空格隔开

```html
<style>
    .red {
        color: red;
    }
    
    .size {
        font-size: 60px;
    }
</style>

<div class="red">hello world</div>
<div class="red size">hello world</div>
```



<output>

<div style="color: red;">hello world</div>

<div style="color: red; font-size: 60px;">hello world</div>

</output>



（3）id选择器

```txt
#元素id {
	属性名: 属性值;
}
```

- 页面中唯一，不能重复
- 一个标签只能有一个id
- id选择器一般与 js 配合使用

```html
<style>
    #name {
        color: green;
    }
</style>

<div id="name">hello world</div>
```


<output>

<div style="color: green">hello world</div>

</output>



（4）通配符选择器

```txt
* {
	属性名: 属性值;
}
```

- 选中页面所有标签
- 一般用于统一页面样式

```css
/* 清除内外边距 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

