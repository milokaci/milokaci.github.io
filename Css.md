# CSS 

CSS 被引入作为一种独立的样式表语言,使得样式和内容能够分开定义和管理.  
CSS 最早是为了更好的渲染 HTML 元素在1996年引入,在 HTML 4 开始使用的.  
* CSS 全称为 (Cascading Style Sheets)  
* 通过将样式规则集中在 CSS 文件中,网页设计师和开发人员能够轻松地修改和应用样式,从而提高了开发效率和网页的可维护性.  

CSS 可以通过以下方式添加到 HTML 中:  
* 内联样式 - 在 HTML 元素中使用"style"属性  
    如:  
    <div style = "background: red;">  
* 内部样式表 - 在 HTML 文档头部 <head> 区域使用 <style> 元素 来包含 CSS  
    如:  
    ```css
    <head>
        <style>
            .class {
                background: red;
            }
        </style>
    </head>
    ```
* 外部引用 - 使用外部 CSS 文件  
    如:  
    <link rel="stylesheet" href="css/style.css">  


CSS 规则由两个主要的部分构成：选择器,以及一条或多条声明  
选择器 {  
    属性1: 值;  
    属性2: 值;  
    属性3: 值;  
    ...  
}  

## CSS 注释

CSS 注释以/*开始,以*/结束,注释用来解释代码,浏览器会忽略它.  

## id 选择器

CSS 中 id 选择器以 "#" 来定义.  
如:
```css
#id1 {
    text-align: center;
    line-height: 20px;
}
```

## class 选择器 

在 CSS 中,类选择器以 . 号显示.  
如:
```css
.class1 {
    width: 100px;
    height: 20px;
    background: red;
}
```
与 id 选择器不同, class选择器 可以在多个元素中使用.  

## 背景 

CSS 背景属性用于定义 HTML 元素的背景.  
CSS 属性定义背景效果:  
* background-color
    如:
    ```css
    body {background-color: red;}
    ```
* background-image
    如:
    ```css
    body {background-image: url('Gif.gif');}
    ```
* background-repeat
    ```css
    no-repeat 不平铺,  
    repeat-x 水平方向平铺,  
    repeat-y 垂直方向平铺.  
    ```
* background-attachment: 背景图像固定或者随着页面的其余部分滚动  
* background-position  
* background-repeat, 等  

当使用简写属性时,即直接使用 background ,属性值的顺序为:  
1. background-color  
2. background-image  
3. background-repeat  
4. background-attachment  
5. background-position  

### 文本颜色 

```css
h1 {color: red;}
h2 {color: #f00}
h3 {color: #ff0000;}
h4 {color: rgb(255, 0, 0);}
```

### 对齐方式 

```css
h1 {
    text-align: left;
} // 左对齐.
h2 {
    text-align: right;
} // 右对齐.
h3 {
    text-align: center;
} // 居中.
h4 {
    text-align: justify;
}
```

### 文本修饰 

```css
h1 {
    text-decoration:overline;
}
h2 {
    text-decoration:underline;
}
h3 {
    text-decoration:line-through;
}
```

### 文本转换 

```css
p.lowercase {
    text-transform:lowercase;
}
p.uppercase {
    text-transform:uppercase;
}
p.capitalize {
    text-transform:capitalize;
}
```

## 字体 

* 通用字体系列 - 拥有相似外观的字体系统组合   
* 特定字体系列 - 特定的字体系列  

### 字体系列

* font-family 属性设置文本的字体系列.  
* font-family 属性应该设置几个字体名称作为一种后备机制.  

### 字体样式   

```css
p.normal {
    font-style:normal;
}
p.italic {
    font-style:italic;
}
p.oblique {
    font-style:oblique;
}
```

### 字体大小 

`p { font-size: 16px; }`    
`p { font-size: 8vw; }`  
`p { font-size: 1.5em; }`  
`p { font-size: 100%; }` /*根据文字自身大小*/  

```css
a: link {
    color: white;
}
a: visited {
    color: red;
}
a: hover {
    color: blue;
}
a: active {
    color: red;
}
```
a: hover 必须跟在 a: link 和 a: visited后面  
a: active 必须跟在 a: hover后面  

文本修饰

```css
a:link {
    text-decoration:none;
}
a:visited {
    text-decoration:none;
}
a:hover {
    text-decoration:underline;
}
a:active {
    text-decoration:underline;
}
```

## 列表 

```css
ul.a {
    list-style-type: circle;
}
ul.b {
    list-style-type: square;
}
ol.c {
    list-style-type: upper-roman;
}
ol.d {
    list-style-type: lower-alpha;
}

ul {
    list-style-type: none;
    padding: 0px;
    margin: 0px;
}
ul li {
    background-image: url(Gif.gif);
    background-repeat: no-repeat;
    background-position: 0px 5px;
    padding-left: 14px;
}
```

## 盒子模型 

* Margin(外边距)  
* Border(边框)  
* Padding(内边距)  
* Content(内容)  

### 边框 

```css
.none {
  border-style: none; /* 无边框 */
}
.dotted {
  border-style: dotted; /* 虚线边框 */
}
.dashed {
  border-style: dashed; /* 虚线边框 */
}
.solid {
  border-style: solid; /* 实线边框 */
}
.double {
  border-style: double; /* 双边框 */
}
.groove {
  border-style: groove; /* 凹槽边框 */
}
.ridge {
  border-style: ridge; /* 垄状边框 */
}
.inset {
  border-style: inset; /* 嵌入边框 */
}
.outset {
  border-style: outset; /* 外凸边框 */
}
.hidden {
  border-style: hidden; /* 隐藏边框 */
}
.mix {
  /* 自定义混合边框样式 */
}
```

### 轮廓 

```css
outline {
    outline-color: ;
    outline-style: ;
    outline-width: ;
}
```

outline-color 包括 (  
    color-name,hex-number,  
    rgb-number,invert,inherit.  
)  

outline-style 包括 (  
    none,dotted,dashed,  
    solid,double,groove,  
    ridge,inset,outset,inherit.  
)  

outline-width 包括 (  
    thin,medium,  
    thick,length,inherit.  
)  

### 外边距 

```css
margin-top: 100px;  
margin-bottom: 100px;  
margin-left: 100px;  
margin-right: 100px;  
```

margin 可以接收1-4个值:  
margin: 1
一个值时,对应上下左右.  
margin: 1,2
二个值时,分别对应上下,左右.  
margin: 1,2,3
三个值时,分别对应上,左右,下.  
margin: 1,2,3,4
四个值时,分别对应上,下,左,右.  

## 尺寸

* height  
* line-height  
* max-height  
* max-width  
* min-height  
* min-width  
* width  
