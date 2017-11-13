# HTML与CSS简单页面效果实例

## 1.1 总体实验概述（结构）

整体效果如下图所示：

![整体效果图]()

首先分析整个网页的结构，可以将整个页面分为三个部分。

第一个部分是头部，上面有标题，导航还有表单，最后有一个小插图。

第二部分是主体，其中有文字描述，有下划线，有图片的排布。

第三部分就是简单的脚部。

用一张结构图可以描述这个页面的结构：

![整体结构图]()

每个模块用一个div来描述就可以实现。

## 1.2 head部分
从结构图上可以看出这个部分要实现的功能比较多，首先定义一个div来承载这样一个标题。


html文件:
````
<div class="headtitle"><h2>Colorful Life</h2></div>
````
后面我们要做的就是加上导航,导航利用列表引入,我们知道列表默认的列表会垂直排布,这里我们需要将其设置成为水平排布,为了美观,我们还需要适当加上
内边据和外边距.
````
<div class="headlead">
               <ul>
                  <li><a href="./cabin.png">Working</a></li>
                   <li><a href="./cake.png">Eating</a></li>
                   <li><a href="./game.png">Playing</a></li>
                   <li><a href="./circus.png">Sleeping</a></li>
               </ul>
</div>
````           
css文件:
````
li{
    padding: 2px;
    display: inline;
}
````
既然是导航,列表元素必定是链接,涉及到链接,我们就要设置,是否去掉下划线,鼠标移动到上面有什么变化,单击之前是什么颜色,点击之后是什么颜色(这里简单设置):
````
a:link,a{
    color: snow;
    text-align: center;
    padding: 2px;
    text-decoration: none;

}
a:hover{
    color: black;
}
````
在右边我们需要插入一个图片,让它浮动在最右边.
````
<div class="headimage">
               <img src="profile.png">
</div>
````
````
.headimage{

    float: right;
    margin-top: 30px;
    margin-right: 5px;
}
.headimage img{
    height: 60px;
    width: 60px;
}
````
这些都是比较简单的设置,前面我们都讲到过的,下面就还剩一个输入文字的表单,只需设置表单设置边框为圆弧,背景颜色,输入类型.

html文件:
````
 <div class="headform">
               <form>
                   <input type="text">
               </form>
</div>
````
css文件：
````
.headform form{
    float: right;
    height: 26px;
    margin-right: 50px;
}

form input{
    height: 20px;
    background-color: cadetblue ;
    width: 100px;
    margin-top: 50px;
    border-radius: 30px;

}
````

## 1.3 body部分
从结构图中我们可以看出,这部分是两大模块,一段的文描述加上下面的图片排列.

首先我们在把文字描述写出来:

html文件:
````
 <div class="bdytitle">
               <h3>enjoy everyday of us</h3>
               <p>let's study with us ,improve with us,we need you</p>
 </div>
 ````
在 css 中我们设定字体颜色模块边距等:
````
.bdytitle{
    color: snow;
}

.bdytitle p{
    margin: 20px;
}
````
下面这部分就是上一节中的图片排版,这里主要涉及到图片的边框,大小,设置浮动.

html文件:
````
<div class="img1">
    <img src="cabin.png">
    <p>Working</p>
</div>
````
css文件:
````
.img1{
    border: 2px solid lightgray;
    float: left;
    text-align: center;
    margin: 10px 10px;
}

.img1 img{
    width: 250px;
    height: 220px;
}

.img1 p{
    color: snow;
    font-size: 20px;
}
````

## 1.4 foot部分
在网页的最后我们加上了一个底框:

html文件:
````
 <div class="foot">
        shiyanlou

</div>
````
     
css文件:
````
.foot{
    text-align: center;
    background-color: lightgray;
    height: 50px;
    padding: 20px;
    font-size: 30px;
    color: darkslategrey;
}
````
 代码参照附件inde.html 和 MyCss.css。
