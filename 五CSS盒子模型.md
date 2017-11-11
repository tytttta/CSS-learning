# CSS盒子模型

## 1.1 CSS盒子模型概述

盒子模型的组成包括： margin（外边距）；border（边框）；padding（内边距）；content（内容）。

正文框的最内部分是实际的内容，直接包围内容的是内边距。内边距呈现了元素的背景。内边距的边缘是边框。边框以外是外边距，外边距默认是透明的。

结构如下图：

![盒子模型的结构图](https://github.com/tytttta/CSS-learning/blob/master/qq.png)

内边距、边框和外边距都是可选的。默认值是零。但是许多元素将由用户单独设置也可以使用通用选择器对所有元素进行设置，相当于一个初始化：
````
*{
  margin:0;
  padding:0;
 }
```` 
从上面的图片可以看出，宽度width和高度height指的是内容区域的宽度和高度。增加内边距、边框和外边距不会影响内容区域的尺寸，但是会增加元素框的总尺寸。

可以设置如下这几个属性：
````
box{
  width:70px;
  margin:10px;
  padding:5px;
 }
 ````
 外边距可以是负值，而且在很多情况下都要使用复制的外边距。
 
 ## 1.2CSS盒子模型内边距
 内边距在正文（content）外，边框（border）内。控制该区域最简单的属性是padding属性。padding属性定义元素边框与元素内容之间的空白区域。
 
 CSS padding属性定义元素的内边距。padding属性接受长度值或百分比值，但不允许使用负值。
 
 可以进行统一的内边距设置，也可以进行单边的内边距设置：
 
 如：如果希望所有h1元素的各边都有10像素的内边距，可以：
 ````
 h1{
  padding:10px;
 }
 ````
 还可以按照**上、右、下、左**的顺序分别设置内边距，各边使用不同的单位或百分比值。
 ````
 h1{
  padding:10px 0.25em 2ex 20%;
  }
  ````
  如果只想设置某一边的内边距，可以通过以下四个属性
  
  - padding-top
  - padding-right
  - padding-botton
  - padding-left
 
 ## 案例
 html文件
 ````
 <table border="1">
    <tr>
        <td>
            <h1>正文</h1>
        </td>
    </tr>
</table>
````
css文件
````
h1 {
    padding-left: 5cm;
    padding-right: 5cm;
    padding-top: 30px;
    padding-bottom: 30px;
}
````
## 1.3 CSS 盒子模型边框
元素的边框是围绕元素内容和内边距的一条或多条线。设置border属性可以规定元素边框的样式、宽度和颜色。

可以通过 **border-style** 设置边框样式，通过 **border-top-width，border-right-width，border-bottom-width，border-left-width** 设置单边边框的宽度，
通过 **border-color** 属性设置边框颜色，一次接受四个值分辨表示边框的四个边。同样可以通过 **border-top/right/bottom/left-color** 设置颜色。

## 1.4 CSS盒子模型外边距
外边距就是围绕内容框的区域，默认是透明的区域。同样可以通过 **margin-top/right/bottom/left** 设置相应上的外边距。

margin的默认值是0， 所以如果没有为margin声明一个值，就不会出现外边距。但是在实际中，浏览器对许多元素已经提供了预定的样式，外边距也不例外。如，在支持CSS
的浏览器中，外边距会在每个段落元素的上面和下面生成“空行”，因此，如果没有为p元素声明外边距，浏览器可能会自己应用一个外边距。

### 值复制
通过值复制可以不必重复输入数字。
如
````
p{margin:0.5em 1em 0.5em 1em;}
````
值复制方式：
````
p{margin:0.5em 1em;}
````
这是因为CSS定义的规则：

**如果缺少左外边距的值，则使用右外边距的值**
**如果缺少下外边距的值，则使用上外边距的值**
**如果缺少右外边距的值，则使用左外边距的值**

即对称复制
````
h1{margin:0.25em 1em 0.5em;} /*等价于0.25em 1em 0.5em 1em*/
h2{margin:0.5em 1em;}/*等价于0.5em 1em 0.5em 1em*/
p{margin:1px;}/*等价于 1px 1px 1px 1px*/
````

### 外边距的合并
合并前和合并后区别如下：

![外边距合并](https://github.com/tytttta/CSS-learning/blob/master/qq2.png)

不同模块之间默认的状态是合并的状态。

## 1.5CSS盒子模型的应用



  

