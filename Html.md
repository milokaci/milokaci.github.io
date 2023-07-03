# HTML

* HTML 全称 HyperText Markup Language,是一种用于创建网页的标准标记语言.  
* HTML 文档包含了 HTML 标签及文本内容,也叫做 web 页面.  

## 标签 

HTML 标记标签通常被称为 HTML 标签 (HTML tag).

1. HTML 标签是由尖括号包围的关键词，比如 &lt;html>.  
2. HTML 标签通常是成对出现的，比如 &lt;b> 和 &lt;/b>.  
3. 标签对中的第一个标签是开始标签，第二个标签是结束标签.  
4. 开始和结束标签也被称为开放标签和闭合标签.  

## 基础

``` html
<html>
    <!-- 定义html文档 -->
    <head>
        
    </head>
    <body>
        <!-- 定义文档主体 -->
    </body>
</html>
```

### 段落 

`<p>Paragraph</p>`  

### 链接 

`<a href = "https://github.com/">GitHub</a>`
* 也可将图片设置为链接
`<a href = "https://github.com/"><img src="img/Img.png"></a>`

### 图像 

`<img src="/images/logo.png" width="64" height="64" />`

### 注释 

`<!-- 注释 -->`

### 元素语法 

* HTML 元素以开始标签起始,以结束标签终止.  
* 元素的内容是开始标签与结束标签之间的内容.  
* 某些 HTML 元素具有空内容.  
* 空元素在开始标签中进行关闭.  
* 大多数 HTML 元素可拥有属性.  

* HTML 元素可以嵌套
```html
<html>
    <body>
        <p>paragraph</p>
    </body>
</html>
```

## 属性 

* 属性可以在元素中添加附加信息.  
* 属性一般描述于开始标签.  
* 属性总是以名称/值对的形式出现.    
* 属性值应当被包括在双引号或单引号内.  

## 超链接 

HTML使用标签 &lt;a>来设置超文本链接。  

语法  
`<a href="url">链接文本</a>`
`<a href="https://github.com/" target="_blank"">github</a>`

## Head 

`<head>` 元素包含了所有的头部标签元素.  
在 `<head>`元素中你可以插入脚本,样式文件,及各种meta信息.  

可以添加在头部区域的元素标签为:  
```
<title>, <style>, <link>, <script>
```
<title> 标签定义了 HTML 文档的标题.它是位于 <head> 元素内的一个标签,用于指定该文档的标题信息.以下是 <title> 标签的一些重要作用:  
* 定义浏览器工具栏的标题: 标签的文本内容将显示在浏览器的标题栏或选项卡上,以便用户可以轻松地识别和区分不同的网页.
* 显示在收藏夹中的标题: 当用户将网页添加到收藏夹或书签时,收藏夹中显示的标题就是标签中指定的文本.  
* 在搜索引擎结果页面中显示的标题: 搜索引擎会将标签中的文本作为网页在搜索结果页面上的标题显示,这对于搜索引擎优化非常重要.  

<link> 标签用于定义文档与外部资源之间的关系,最常见的用途是链接到样式表文件.  
通过指定 <link> 标签的 rel 属性为 "stylesheet",可以将外部样式表文件与 HTML 文档关联起来.  

在`<style>` 元素中你也可以直接添加样式来渲染 HTML 文档:  
```html  
<head>
    <style type="text/css">
        body {
            background-color:yellow;
        }
        p {
            color:blue
        }
    </style>
</head>
```

为搜索引擎定义关键词:  
`<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">`
为网页定义描述内容:  
`<meta name="description" content="Web">`
定义网页作者:  
`<meta name="author" content="Runoob">`
每30秒钟刷新当前页面:  
`<meta http-equiv="refresh" content="30">` 

## 使用CSS 

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

## 图像 

在 HTML 中，图像由`<img>` 标签定义.  
`<img>` 是空标签,意思是说,它只包含属性,并且没有闭合标签.  
要在页面上显示图像，你需要使用源属性.
src 指 "source",源属性的值是图像的 URL 地址.  
`<img src="url" alt="some_text">`
alt 属性用来为图像定义一串预备的可替换的文本.  
在无法加载图像时, 这串文字可以告诉别人图片的大致内容.  

设置宽度(默认单位为像素)  
`<img src="pulpit.jpg" alt="Pulpit rock" width="304" height="228">`  

## 表格 

表格是由 <table> 标签来定义的.  
每个表格由若干行组成,每行由 <tr> 标签定义.  
而每行又被分割为若干单元格,单元格由 <td> 标签定义.  
字母 "td" 代表表格数据,也就是数据单元格的内容.  
数据单元格可以包含各种内容,例如文本、图片、列表、段落、表单、水平线.  
表格的表头通常使用 <th> 标签进行定义,它与 <td> 类似,但其目的是标识表格的列标题.  
```html
<table border="1">
    <tr>
        <th>Num1</th>
        <th>Num2</th>
    </tr>
    <tr>
        <td>100</td>
        <td>200</td>
    </tr>
    <tr>
        <td>1000</td>
        <td>2000</td>
    </tr>
</table>
```

## 列表 

### 无序列表 

无序列表使用 `<ul>` 标签.  
列表项起始于 `<li>` 标签.  
```html
<ul>
    <li>1</li>
    <li>2</li>
</ul>
```

### 有序列表 

有序列表始于 `<ol>` 标签.  
列表项起始于 `<li>` 标签.  

```html
<ol>
    <li>1</li>
    <li>2</li>
</ol>
```

## 布局 

使用HTML <table>标签确实是创建布局的一种简单方式,特别适用于创建多列的布局.  

```html
<body>
    <tr> <!-- 行1 -->
        <td>
            <!-- 列1 -->
        </td>
        <td>
            <!-- 列2 -->
        </td>
    </tr>
</body>

```

## 表单和输入 

我们可以使用 `<form>` 标签来创建表单:  
```html
<form action="">
Username: <input type="text" name="user"><br>
Password: <input type="password" name="password">
</form>
```  

* `<input type="radio">` 标签定义了表单的单选框选项  
```html
<form action="">
    <input type="radio" name="sex" value="male">男<br>
    <input type="radio" name="sex" value="female">女
</form>
```

* `<input type="checkbox">` 定义了复选框  
```html
<form>
    <input type="checkbox" name="vehicle" value="Bike">1<br>
    <input type="checkbox" name="vehicle" value="Taxi">2
</form>
```

* `<input type="submit">` 定义了提交按钮  
```html
<form name="input" action="html_form_action.php" method="get">
    Username: <input type="text" name="user">
    <input type="submit" value="Submit">
</form>
```

## 框架 

通过使用框架,可以在同一个浏览器窗口中显示不止一个页面.  

`<iframe src="URL"></iframe>` URL指向不同的网页.  

frameborder 表示是否显示边框,设置属性值为 "0" 移除iframe的边框.  
`<iframe src="demo_iframe.htm" frameborder="0"></iframe>`  

iframe 可以显示一个目标链接的页面,   
目标链接的属性必须使用 iframe 的属性,如下实例:   
```html
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="https://www.runoob.com" target="iframe_a" rel="noopener">RUNOOB.COM</a></p>
```

## 统一资源定位器(Uniform Resource Locators) 

* scheme - 定义因特网服务的类型,最常见的类型是 http.  
* host - 定义域主机    
* domain - 定义因特网域名,比如 runoob.com.    
* :port - 定义主机上的端口号.  
* path - 定义服务器上的路径.  
* filename - 定义文档/资源的名称.  
