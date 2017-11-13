# CSS基本样式（二）

## 1.1 CSS链接

在CSS的链接属性设置中，我们能设置color，font-family，background等。

### 1.1.1 CSS链接的四种状态：

a:link ---普通的，未被访问的链接

a:visited ---用户已访问的链接

a:hover ---鼠标指针位于链接的上方

a:active ---链接被点击的时刻

#### 案例

index.html文件
````
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title>css test</title>
    <link rel="stylesheet" type="text/css" href="test.css">
</head>
<body >

<a href="http://www.shiyanlou.com">shiyanlou</a>

</body>
</html>
````
MyCss.css文件
 
````
a:link {color:#FF0000;}    /* 未被访问的链接 */
a:visited {color:#00FF00;} /* 已被访问的链接 */
a:hover {color:#FF00FF;}   /* 鼠标指针移动到链接上 */
a:active {color:#0000FF;}  /* 正在被点击的链接 */
````

这四个属性要遵循的顺序问题：

1. a:hover必须位于a:link和a:visited之后

2. a:active必须位于a:hover之后

### 1.1.2 CSS 设置链接背景颜色

修改对应的属性background-color即可。

````
a:link {background-color:#B2FF99;}
a:visited {background-color:#FFFF85;}
a:hover {background-color:#FF704D;}
a:active {background-color:#FF704D;}
````

### 1.1.3修改链接下划线

在link 属性中加入text-decoration属性，将传值改为“none”即可去掉下划线。


## 1.2 CSS列表

CSS列表允许防止，改变列表标志，或者将图片作为列表项标志。

### 1.2.1 列表类型

列表有无序、有序之分，无序列表又可以用不同的标记来区分。而list-style-type这个属性可以用来控制标记类型。

index.html文件
````
<ul class="circle">
    <li>shiyanlou</li>
    <li>shiyanlou</li>
</ul>

<ul class="square">
    <li>shiyanlou</li>
    <li>shiyanlou</li>
</ul>

<ol class="upper-roman">
    <li>shiyanlou</li>
    <li>shiyanlou</li>
</ol>

<ol class="lower-alpha">
    <li>shiyanlou</li>
    <li>shiyanlou</li>
</ol>
````

MyCSS.css文件
````
ul.circle {list-style-type:circle}
ul.square {list-style-type:square}
ol.upper-roman {list-style-type:upper-roman}
ol.lower-alpha {list-style-type:lower-alpha}
```` 

### 1.2.2 列表项图片

在工程文件夹中法如一个小图标，然后在css中添加
```
ul.img1{list-style-image:url("4.ico")}
ul.img2{list-style-image:url("11.ico")}
````

url中是图片名称。

html文件中需要添加：
````
<ul class="img1">
  <li>shiyanlou1</li>
  <li>shiyanlou2</li>
</ul>

<ul class="img2">
  <li>shiyanlou3</li>
  <li>shiyanlou4</li>
</ul>
````

### 1.2.3 简写列表样式

简写列表样式就是把所有用于列表的属性设置于一个声明中。
````
li{list-style:url(image.gif) square}
````
list-style的只可以按任何顺序列出，而且这些值都可以忽略。只要提供了一个值，其他的值就会填入默认值。


## 1.3 CSS表格
在表格学习中需要了解一下属性：

border-collapse --- 设置是否把表格边框合并为单一的边框

border-spacing --- 设置分隔单元格边框的距离

border-sider --- 设置表格标题的位置

empty-cells --- 设置是否显示表格中的空单元格

table-layout --- 设置显示单元、行和列的算法。

### 案例：

html文件：
````
<table id="tb">
    <tr>
        <th>name</th>
        <th>age</th>
        <th>number</th>
    </tr>

    <tr>
        <td>li</td>
        <td>3</td>
        <td>4</td>
    </tr>

    <tr class="tr2">
        <td>li</td>
        <td>3</td>
        <td>4</td>
    </tr>

    <tr>
        <td>li</td>
        <td>3</td>
        <td>4</td>
    </tr>

    <tr class="tr2">
        <td>li</td>
        <td>3</td>
        <td>4</td>
    </tr>

</table>
````
这是是无边框的效果，在css中加入边框并指定颜色

css文件：

````
#tb,tr,th,td{
    border: 1px solid green;
}
````

我们可以通过CSS来定制列表。首先，使用border-collapse让整个列表边框合并为单线，在使用width、height来定制表格大小，之后用background-color加上背景颜色，
text-align设置字符对齐方式，padding设置内边距。

````
#tb td,th{
  border:1px solid greed;
  padding:5px;
 } 
 #tb{
  border-collapse:collapse;
  width:500px;
  text-align:center;
}
# tb th{
  text-align:center;
  color:black;
  background-color:lightseagreen;
}
#tb tr.tr2 td{
  color:black;
  background-color:red;
}
````

## 1.4 轮廓
轮廓是绘制于元素周围的一条线，位于边框边缘的外围，可以起到突出元素的作用。

CSS outline属性规定元素轮廓的样式、颜色和宽度。涉及的属性有：

outline-color --- 设置轮廓的颜色

outline-style --- 设置轮廓的样式

outline-widht --- 设置轮廓的宽度

### 案例：
HTML文件

````
<p id="p1">shiyanlou1</p>
<p id="p2">shiyanlou2</p>
````

CSS 文件

````
#p1{
  outline-color:red;
  outline-style:groove;
  outline-width:10px;
}
#p2{
  outline-color:green;
  outline-style:dotted;
  outline-width:5px;
}
````
