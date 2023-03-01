# CSS 装饰

## 1. 垂直对齐 vertical-align

基线(baseline)：浏览器文字类型元素排版中存在用于对齐基线

| 属性值   | 效果           |
| -------- | -------------- |
| baseline | 默认，基线对齐 |
| top      | 顶部对齐       |
| middle   | 中部对齐       |
| bottom   | 底部对齐       |

```css
vertical-align: middle

```

示例：

[](./demo/css-decorate-1.html ':include :type=code')

[](./demo/css-decorate-1.html ':include height=80')



> 浏览器把行内和行内块当做文字处理，文字默认基线对齐

示例一：输入框垂直居中对齐

[](./demo/css-decorate-2.html ':include :type=code')

[](./demo/css-decorate-2.html ':include height=100')




示例二：图片垂直居中对齐

[](./demo/css-decorate-3.html ':include :type=code')

[](./demo/css-decorate-3.html ':include height=270')


示例三：图片水平垂直居中

[](./demo/css-decorate-4.html ':include :type=code')

[](./demo/css-decorate-4.html ':include height=420')


## 2. 光标类型 cursor

| 属性值  | 效果                 |
| ------- | -------------------- |
| default | 默认，箭头           |
| pointer | 小手，提示可点击     |
| text    | 工字型，提示可选择   |
| move    | 十字光标，提示可移动 |



[](./demo/css-decorate-cursor.html ':include :type=code')

[](./demo/css-decorate-cursor.html ':include height=150')



## 3. 边框圆角 border-radius

```css
/* 单值 4个角一样*/
border-radius: 数字px/百分比;

/* 多值 左上角开始，顺时针赋值，没有赋值看对角*/
border-radius: 左上 右上 右下 左下;Copy to clipboardErrorCopied
```

（1）正圆

- 盒子必须是正方形
- 设置边框圆角为盒子宽高的一半

示例：

[](./demo/css-decorate-radius-1.html ':include :type=code')

[](./demo/css-decorate-radius-1.html ':include height=250')



```css
/* 最大值 50% */
border-radius: 50%;Copy to clipboardErrorCopied
```

（2）胶囊按钮

- 盒子设置为长方形
- 设置边框圆角为高度的一半

```css
border-radius: height/2;
```

示例：

[](./demo/css-decorate-radius-2.html ':include :type=code')

[](./demo/css-decorate-radius-2.html ':include height=80')


## 4. 溢出部分效果 overflow

溢出部分：盒子内容部分超出盒子范围的区域

| 属性值  | 效果                               |
| ------- | ---------------------------------- |
| visible | 默认，溢出部分可见                 |
| hidden  | 溢出部分隐藏                       |
| scroll  | 无论是否溢出都显示滚动条           |
| auto    | 根据是否溢出，自动显示或隐藏滚动条 |

示例：

[](./demo/css-decorate-overflow.html ':include :type=code')

[](./demo/css-decorate-overflow.html ':include height=120')


## 5. 元素本身隐藏]

```css
/* 占位隐藏 */
visibility: hidden;

/* 不占位隐藏（常用） */
display: none;
```

[](./demo/css-decorate-visibility-1.html ':include :type=code')

[](./demo/css-decorate-visibility-1.html ':include height=220')



示例：默认隐藏 鼠标悬停显示

[](./demo/css-decorate-visibility-2.html ':include :type=code')

[](./demo/css-decorate-visibility-2.html ':include height=220')


## 6. 元素整体透明 opacity

属性值：

- 0-1 之间的数字；
- 0 完全透明，1 完全不透明

示例：

[](./demo/css-decorate-opacity-1.html ':include :type=code')

[](./demo/css-decorate-opacity-1.html ':include height=120')

> 使用opacity 盒子里面的元素也会透明


## 7.半透明

```css
background-color: rgba(0, 0, 0, 0.5);

```

示例：

[](./demo/css-decorate-opacity-2.html ':include :type=code')

[](./demo/css-decorate-opacity-2.html ':include height=120')