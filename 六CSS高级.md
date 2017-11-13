# CSS高级

## 1.1 CSS定位
定位允许定义元素框相对于其正常位置应该出现的位置，或者相对于父元素、另一个元素甚至浏览器本身的位置。

CSS有三种定位机制

- 普通流：
元素按照其在HTML中的位置顺序决定排布的过程
- 浮动：
浮动的框可以向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。
- 绝对定位：
绝对定位使元素的位置与文档流无关，一次不占据空间。这一点与相对定位不同，相对定位实际上被看做普通流定位模型的一部分，因此元素的位置相对于它在普通流中的
位置。

定位属性：

position：将元素放在一个静态的，相对的，绝对的或固定的位置。

通过对top，left，right，bottom这四个属性的赋值让元素相对应的方向偏移。

overflow设置元素溢出其区域发生的事情。

clip设置元素的显示形状，多用于图片。

vertical-align设置元素的垂直方式

z-inex设置元素的堆叠顺序

### 案例1：position属性：

HTML文件
````
<div class="position1"></div>
<p>this is shiyanlou</p>
<p>this is shiyanlou</p>
<p>this is shiyanlou</p>
<p>this is shiyanlou</p>
````
CSS文件
````
.position1{
    width: 100px;
    height: 100px;
    background-color: cornflowerblue;
    
    /*以上是普通流的效果，加上position属性，向左偏移60px。
    */
 position: relative;
 left: 60px;

}
````

再将position位置设为绝对：
````
position: absolute;
````
还有两个属性是fixed和static。fixed是将元素固定下来，就算屏幕滚动元素也会在同一个地方不动，static设置后，偏移量将不起作用。


### 案例2： 再加一个块在div后面
HTML文件：
````
<div class="position1"></div>
<div class="position2"></div>
````

CSS文件：
````
.position2{
    width: 100px;
    height: 100px;
    background-color: aquamarine;
    position: relative;
    left:10px;
    top: 10px;
}
````

## 1.2 CSS浮动
涉及到的属性是float，可以赋值为：

left：元素向左浮动

right：元素向右浮动

none：不浮动

inherit：从父级继承浮动的属性

clear：用于去掉个方向的浮动属性（包括继承的属性）

###  案例
HTML文件
````
  <div class="qd"></div>
  <div class="wd"></div>
  <div class="ed"></div>
````
CSS文件
````
.qd{
    width: 100px;
    height: 100px;
    background-color: lightskyblue;
}
.wd{
    width: 100px;
    height: 100px;
    background-color: lightseagreen;

}
.ed{
    width: 100px;
    height: 100px;
    background-color: lightsalmon;

}
````
在这基础上给它们加上float属性。
````
float:left/right;
````
去除浮动效果：
````
.id{
  clear:both;
  }
````

## 1.3 CSS 尺寸
尺寸属性允许控制元素的高度和宽度。同样，它允许增加行间距。涉及的属性有：

height --- 设置元素的高度

line-height --- 设置行高
 
max-height --- 设置元素的最大高度

max-width --- 设置元素的最大宽度

min-height --- 设置元素的最小高度

min-width --- 设置元素的最小宽度

width --- 设置元素的宽度

### 案例
css文件
````
.p1{
    line-height: normal;
    width: 400px;
}
.p2{
    line-height: 50%;
    width: 400px;
}
.p3{
    line-height: 200%;
   width: 400px;
}
````
## 1.4 CSS 导航栏
不管是什么网页都会有导航栏来表示本网页所包含的内容，一般导航栏分为水平导航栏和垂直导航栏。

###  垂直导航栏
首先以列表形式最为最基础的承载，然后加入链接。
````
<ul>
    <li><a href="http://www.shiyanlou.com">shiyanlou1 link</a></li>
    <li><a href="http://www.shiyanlou.com">shiyanlou2 link</a></li>
    <li><a href="http://www.shiyanlou.com">shiyanlou3 link</a></li>
    <li><a href="http://www.shiyanlou.com">shiyanlou4 link</a></li>
</ul>
````
首先去掉前面的点
````
ul{
  list-style:none;
  }
````
接下来去掉下划线（不管是未点击状态还是点击状态都去掉），加上背景颜色，再将其作为快来显示。
````
a:link, a:visited{
  text-decoration:none;
  background-color:lightgray;
  display:block;
}
````
最后再给导航栏加个鼠标移动到上面时，该表背景颜色
````
a:active,a:hover{
  background-color:cadetblue;
}
````

### 水平导航栏
首先要将前面显示效果删除
````
display:none;
````
然后只需要在li标签改变显示方式就可以：
````
li{
  display:inline;
}
````

## 1.5 CSS 图片
首先引入一张图片，使用div承载
````
<div class="image">
        <a href="./11.jpg" target="_self">
            <img src="11.jpg" width="150px" height="150px">
        </a>
        <div class="text">beautiful</div>
 </div>
````
接下来开始定制图片的显示：
图片加边框，修改描述字体中对齐，修改字体大小，将整个div向左移动，是边框与图片进行贴合。
````
.image{
    border: 2px solid darkgrey;
    width: auto;
    height: auto;
    float: left;
    text-align: center;
    padding: 5px;
}
img{
    padding: 5px;
}
.text{
    font-size: 20px;
    margin-bottom: 5px;
}
````
可以继续设计图片透明度：
````
opacity:0.5;
````
这个属性的值范围为0-1,0为完全透明，1代表完全不透明。

 
