# CSS 盒模型



## 盒子模型

（1）盒子

标签可以看作是一个盒子

（2）盒子模型：

- 外边距区域 margin
- 边框区域 border
- 内边距区域 padding
- 内容区域 content

（3）盒子内容的宽高

- width
- height

```css
.box {
    width: 100px;
    height: 100px;
}
```



## 边框 border

```css
/* 粗细 线条样式 颜色（不分先后顺序）*/
/* 默认4个方向都有*/
border: 10px solid red;

/* 单个方向 */
border-top: 10px solid red;
border-bottom: 10px solid red;
border-left: 10px solid red;
border-right: 10px solid red;

/* 单个属性 */
border-width: 边框粗细
border-style: 边框样式
border-color: 边框颜色
```

线条可选样式

- solid 实线
- dashed 虚线
- dotted 点线

布局顺序：从外到内，从上到下



## 内边距 padding

```css
/* 可取 4 个值、3 个值、2 个值、1 个值 */
padding: 上 右 下 左;
padding: 上 左右 下;
padding: 上下 左右;
padding: 上下左右;

/* 单个方向 */
padding-top: 10px;
padding-bottom: 10px;
padding-left: 10px;
padding-right: 10px;
```

规律：顺时针，值不够看对边



## 导航实例

[](./demo/css-box-1.html ':include :type=code')

[](./demo/css-box-1.html ':include height=80')



## 盒子尺寸计算

```
box-sizing: content-box 默认
盒子最终宽度 = width(content) + padding + border

/* 自减模式 */
box-sizing: border-box
盒子最终宽度 = width = padding + border + content
```



## 外边距 margin

设置值的方式和 padding 类似

```css
/* 可取 4 个值、3 个值、2 个值、1 个值 */
margin: 上 右 下 左;
margin: 上 左右 下;
margin: 上下 左右;
margin: 上下左右;

/* 单个方向 */
margin-top: 10px;
margin-bottom: 10px;
margin-left: 10px;
margin-right: 10px;
```

使用 margin 让元素居中

```css
.box {
 margin: 0 auto;   
}
```



## 清除浏览器默认样式

京东

```css
* {
    margin: 0;
    padding: 0;
}
```

淘宝

```css
blockquote,
body,
button,
dd,
dl,
dt,
fieldset,
form,
h1,
h2,
h3,
h4,
h5,
h6,
hr,
input,
legend,
li,
ol,
p,
pre,
td,
textarea,
th,
ul {
  margin: 0;
  padding: 0;
}

```

常用的清除样式

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

```

去掉列表前的符号

```css
ul {
  list-style: none;
}

```



## 外边距折叠现象

- 合并现象
- 塌陷现象

（1）合并现象

- 场景：垂直布局的块级元素，上下的 margin 会合并
- 结果：最终两者距离为 margin 的最大值
- 解决方法：只给其中一个盒子设置 margin

[](./demo/css-box-2.html ':include :type=code')

[](./demo/css-box-2.html ':include height=400')

（2）塌陷现象

- 场景：相互嵌套的`块级`元素，子元素的 margin-top 会作用在父元素上
- 结果：导致父元素一起往下移动
- 解决方法：

1. 给父元素设置 border-top 或者 padding-top(分隔父子元素的 margin-top)
2. 给父元素设置 overflow: hidden;
3. 转换为行内块元素
4. 设置浮动

[](./demo/css-box-3.html ':include :type=code')

[](./demo/css-box-3.html ':include height=600')



## 行内标签的 margin/padding

垂直方向不生效，使用行高 line-height 实现

[](./demo/css-box-4.html ':include :type=code')

[](./demo/css-box-4.html ':include height=60')

## 综合案例

[](./demo/css-box-5.html ':include :type=code')

[](./demo/css-box-5.html ':include height=450')