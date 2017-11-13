# CSS选择器

## 1.1 元素选择器
最常见的就是元素选择器，文档的元素就是最基本的选择器，就像h1{}，a{}等。

## 1.2 选择器分组
```
h1,h2,h3,h4{
  color:red;
}
```
还有种方式是选择通配符
````
*{
  color:red;
}
````
这么一来如果没有特定的元素的设置，都会发生颜色的转换。 如果希望某个元素和其它元素不同，只需要进行覆盖即可。如：
````
h4{
  color:green;
}
````
一般使用通配符的时候是设置整个页面的内边距和外边距，如下：
````
#{
  padding:0px;
  margin:0px;
}
````

## 1.3 类选择器
类选择器允许以一种独立于文档元素的方式来制定样式。用.classname{}形式。

HTML文件
````
<div class="div">aaaa</div>
````
CSS文件
````
.div{
  color:red;
 }
````
将元素选择器和类选择器结合的方式
````
h1.div{
  color:greed;
}
````

多类选择器
css文件：
````
.p1.p2{
  font-style:italic;
}
````
html文件：
````
<p class="p1 p2">kdkkdk</p>
````

## 1.4 id 选择器
id选择器类似于类选择器。使用方式是“# id名{}”。

html文件
````
<p id="div"> dkfj</p>
````
css文件
````
#div{
  color:blue;
}
````
区别：
1. id在文档中只能使用一次，而类可以使用多次。 
2. id选择器不能像类选择器一样结合使用

## 1.5 属性选择器
简单的属性选择器，如[title]{}
HTML文件,在head中添加：
````
<style>
[title]{

        color: cadetblue;
    }
</style>
````
在body中加入一个p标签：
````
<p title="li">badfjs</p>
````
**属性选择器还可以根据具体的属性值进行选择**，案例：

head中添加：
````
a[href="http://www.shiyanlou.com"]{
        color: cornflowerblue;

        }
````
body中添加：
````
<a href="http://www.shiyanlou.com">shiyanlou right</a>
<a href="http://www.baidu.com">baidu</a>
````

## 1.6 后代选择器
后代选择器可以选择作为某元素后代的元素。

### 案例：
首先在body中添加一个p标签，并在里面嵌套一个strong子标签：
````
<p>shiyanlou is <strong>it</strong> website</p>
````
然后将it这个单词设置颜色，其它的不变，可以在CSS文件中使用后代选择器
````
p strong{
  color:yellow;
}
````

## 1.7 子元素选择器
与后代选择器相比，子元素选择器只能选择作为某子元素的元素。

HTML文件：
````
<h1>shiyanlou is a <strong>it</strong> website</h1>
````

CSS文件：
````
h1 > strong{
  color:gray;
  font-size:60px;
}
````

## 1.8 相邻兄弟选择器
相邻兄弟选择器可以选择紧接在另一个元素后的元素，且二者有相同的父级，示例：h1+p{}。

兄弟选择器多用于列表，具有相同的父级元素ul。

html文件
````
<ul>
    <li>shiyanlou</li>
    <li>shiyanlou</li>
    <li>shiyanlou</li>
</ul>
````

CSS文件:
````
li+li{
    color: cadetblue;
    font-size: 40px;
}
````

