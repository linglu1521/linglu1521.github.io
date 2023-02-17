## 背景颜色

```css
/* 默认背景颜色是透明，背景色在背景图之下 */
background-color: transparent;
```

示例：

```html
<style>
    .box {
        width: 100px;
        height: 50px;
        background-color: pink;
    }
</style>

<div class="box"></div>
```

[](demo/css-background-1.html ':include height=100')

## 背景图片

```css
background-image: url(图片路径);
```

示例：

```html
<style>
    .box {
        width: 600px;
        /* 元素必须给一个尺寸才能显示背景图 */
        height: 500px;
        background-image: url(/blog/html-basic/demo/images/k.gif)
    }
</style>

<div class="box"></div>
```

[](demo/css-background-2.html ':include height=300')

## 背景平铺

background-repeat

| 取值      | 效果                           |
| --------- | ------------------------------ |
| repeat    | （默认值）水平和垂直方向都平铺 |
| no-repeat | 不平铺                         |
| repeat-x  | 水平方向平铺（x轴）            |
| repeat-y  | 垂直方向平铺（y轴）            |

示例：

```html
<style>
    .box {
        width: 600px;
        /* 元素必须给一个尺寸才能显示背景图 */
        height: 500px;
        background-image: url(/blog/html-basic/demo/images/k.gif)
        background-repeat: no-repeat;
    }
</style>

<div class="box"></div>
```

[](demo/css-background-3.html ':include height=300')

## 背景位置

```css
background-position: 水平方向位置 垂直方向位置;
```

属性值

方位名词（最多只能表示9个位置）

- 水平方向：left	center	right
- 垂直方向：top    center    bottom

数字+px（坐标）

- 坐标轴原点(0, 0)在盒子的左上角
- x 轴 水平方向
- y 轴 垂直方向
- 图片左上角与坐标原点重合

示例：

```html
<style>
    .box {
        width: 600px;
        /* 元素必须给一个尺寸才能显示背景图 */
        height: 500px;
        background-image: url(/blog/html-basic/demo/images/k.gif)
        background-repeat: no-repeat;
        background-position: center;
    }
</style>

<div class="box"></div>
```

[](demo/css-background-4.html ':include height=300')

## 背景属性简写

```css
/* 不分先后顺序 */
background: color image repeat position;
```

示例：

```html
<style>
    .box {
        width: 600px;
        /* 元素必须给一个尺寸才能显示背景图 */
        height: 500px;
        /*
        两种写法等价
        background-color: pink;
        background-image: url(/blog/html-basic/demo/images/k.gif)
        background-repeat: no-repeat;
        background-position: center;
        */
        background: pink url(/blog/html-basic/demo/images/k.gif) no-repeat center;
    }
</style>

<div class="box"></div>
```

[](demo/css-background-5.html ':include height=300')

## img标签和背景图片区别

img

- 不设置高度会默认显示
- 重要突出的图会用img

background-image

- 需要设置元素尺寸
- 装饰性图片使用背景图