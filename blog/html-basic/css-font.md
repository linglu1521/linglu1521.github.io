# CSS 字体和文本样式

## 字体大小

```css
/* 浏览器默认字体大小 16px */
font-size: 16px;
```

```html
<div style="font-size: 16px">Hello World!!!</div>
<div style="font-size: 30px">Hello World!!!</div>
```

<output>

<div style="font-size: 16px">Hello World!!!</div>
<div style="font-size: 30px">Hello World!!!</div>

</output>

## 字体粗细

```css
font-weight: 400;
```

| 属性值（单词） | 属性值（数字） | 效果 |
| -------------- | -------------- | ---- |
| normal         | 400            | 正常 |
| bold           | 700            | 加粗 |

- 一般使用数字表示法

```html
<div style="font-weight: 400">Hello World!!!</div>
<div style="font-weight: 700">Hello World!!!</div>
```

<output>

<div style="font-weight: 400">Hello World!!!</div>
<div style="font-weight: 700">Hello World!!!</div>

</output>

## 字体样式

```css
font-style: normal;
```

| 属性值 | 效果 |
| ------ | ---- |
| normal | 正常 |
| italic | 倾斜 |

```html
<div style="font-style: normal">Hello World!!!</div>
<div style="font-style: italic">Hello World!!!</div>
```

<output>

<div style="font-style: normal">Hello World!!!</div>
<div style="font-style: italic">Hello World!!!</div>

</output>

## 字体系列

```css
/* 优先使用：微软雅黑 > 黑体 */
/* 如果没有这些字体就选择一种无衬线字体（sans-serif） */
font-famliy: 微软雅黑, 黑体, sans-serif；
```

| 操作系统 | 默认字体    |
| :------- | ----------- |
| Windows  | 微软雅黑    |
| Mac      | PingFang SC |

常见字体系列

| 常见字体系列             | 特点                               | 场景         | 该系列常见字体        |
| ------------------------ | ---------------------------------- | ------------ | --------------------- |
| 无衬线字体（sans-serif） | 文字笔画粗细均匀，并且首尾无装饰   | 网页         | 黑体、Arial           |
| 衬线字体（serif）        | 文字笔画粗细不均匀，并且首尾有装饰 | 报刊书籍     | 宋体、Times New Roman |
| 等宽字体（monospace）    | 每个字母或文字的宽度相等           | 程序代码编写 | Consolas、 fira Code  |

```html
<div style="font-family: 微软雅黑, 黑体, sans-serif">Hello World!!!</div>
<div style="font-family: 宋体, Times New Roman, serif">Hello World!!!</div>
<div style="Consolas, fira Code, monospace">Hello World!!!</div>
```

<output>

<div style="font-family: 微软雅黑, 黑体, sans-serif">Hello World!!!</div>
<div style="font-family: 宋体, Times New Roman, serif">Hello World!!!</div>
<div style="Consolas, fira Code, monospace">Hello World!!!</div>

</output>

## 文本缩进

```css
/* 首行缩进2个字符 */
text-indent: 2em;
```

取值

- 数字 + px
- 数字 + em（推荐：1em = 当前标签的 font-size 大小）

```html
<p>Hello World!!!</p>
<p style="text-indent: 2em;">Hello World!!!</p>
```

<output>

<p>Hello World!!!</p>
<p style="text-indent: 2em;">Hello World!!!</p>

</output>

## 文本水平对齐方式

```css
text-align: center;
```

| 属性值 | 效果           |
| ------ | -------------- |
| left   | 左对齐（默认） |
| center | 居中对齐       |
| right  | 右对齐         |

可居中的标签

- 文本
- span    a
- input    img

内容居中需要给`父元素`设置居中属性

```html
<p>Hello World!!!</p>
<p style="text-align: center;">Hello World!!!</p>
<p style="text-align: right">Hello World!!!</p>
```

<output>

<p>Hello World!!!</p>
<p style="text-align: center;">Hello World!!!</p>
<p style="text-align: right">Hello World!!!</p>

</output>

## 文本修饰

```css
/* 常用于清除a标签默认下划线 */
text-decoration: none;
```

| 属性值       | 效果   |
| ------------ | ------ |
| underline    | 下划线 |
| line-through | 删除线 |
| overline     | 上划线 |
| none         | 无     |

```html
<p style="text-decoration: underline">Hello World!!!</p>
<p style="text-decoration: line-through">Hello World!!!</p>
<p style="text-decoration: overline">Hello World!!!</p>
<a href="#" style="text-decoration: none">Hello World</a>
```

<output>

<p style="text-decoration: underline">Hello World!!!</p>
<p style="text-decoration: line-through">Hello World!!!</p>
<p style="text-decoration: overline">Hello World!!!</p>

<a href="#" style="text-decoration: none">Hello World</a>

</output>

## 行高

```css
line-height: 1.5;
```

取值

- 数字 + px
- 倍数（当前标签 font-size 的倍数）

文本高度

- 上间距
- 文本高度
- 下间距

应用：

- 单行文本垂直居中：line-height = 元素父元素高度
- 取消上下间距：line-height=1

```html
<p style="line-height: 1;">Hello World!!!</p>
<p style="line-height: 1.5;">Hello World!!!</p>
<p style="line-height: 3;">Hello World!!!</p>
```

<output>

<p style="line-height: 1;">Hello World!!!</p>
<p style="line-height: 1.5;">Hello World!!!</p>
<p style="line-height: 3;">Hello World!!!</p>

</output>

## font 属性简写

复合属性

```css
font: [font-style font-weight] font-size/line-height font-family;
```

在线配置font简写形式

[https://developer.mozilla.org/en-US/docs/Web/CSS/font#live_sample](https://developer.mozilla.org/en-US/docs/Web/CSS/font#live_sample)

```html
<div style="font: italic 700 24px/3 微软雅黑, 黑体, san-serif;">Hello World!!!</div>
```

<output>

<div style="font: italic 700 24px/3 微软雅黑, 黑体, san-serif;">Hello World!!!</div>

</output>