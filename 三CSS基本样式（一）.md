# CSS基本样式（一）

## 1.1 CSS背景
  
CSS允许使用纯色作为背景，也允许使用背景图像创建相当复杂的的效果

| 属性                 | 描述                                |
|-----                |----                                 |
|background-attachment|背景图像是否固定或随着页面的其余部分滚动 |
|background-color|设置元素的背景颜色|
|background-image|把图片设置为背景|
|background-position|设置背景图片的起始位置|
|background-repeat|设置背景图片是否及如何重复|

### 案例1：背景颜色

index.html文件

    <html>
      <head>
          <meta charset="UTF-8">
          <title></title>
          <link rel="stylesheet" href="Mycss.css" type="text/css">
      </head>
      <body>
          <p>I love shiyanlou</p>
      </body>
    </html>

MyCss.css文件

    body{
     background-color: red;
    }

    p{
      width: 150px;
      padding: 10px;
      background-color: #0014ff;
    }

### 案例2：设置背景图

需要在工程文件夹下放置一张图片，用于css设置背景是的引用

MyCss.css文件

    body{
     background-image: url("python.png")
    }

结果可以看到背景图有多个图片，这是因为默认背景图显示重复，可以通过background-repeat设置图片是否可以重复

MyCs.css文件

    body{
        background-image: url("python.png");
        background-repeat: no-repeat;
    }

background-position设置图片的起始位置

    background-position:center top;
    
将背景图从中间顶部放置
    

###  背景关联

如果网页比较长，那么当网页向下滚动时，背景图像也会随之滚动，当网页滚动到超过图像的位置时，图像就会消失。可以通过background-attachment属性防止这种滚动，通过这个属性可以声明图像相对于可视区是固定的。

````
body{
   background-image: url("python.png");
   background-repeat: no-repeat;
   background-attachment:fixed;
}
````

##  CSS3 背景

|属性| 描述|
|----|----|
|background-size|规定背景图片的尺寸|
|background-origin|规定背景图片的定位区域|
background-clip|规定背景的绘制区域|


### 案例
````
body{
   background-image: url("python.png");
   background-repeat: no-repeat;
   background-size：100px 100px;
   /\*图片大小设置成为 100px*100px\*/
}
````

##  CSS样式-文本

### CSS文本属性可以定义文本的外观

通过文本属性可以改变文本的颜色，字符间距，对齐文本，装饰文本，对文本进行缩进等。

|属性|描述|
|----|----|
|color|文本颜色|
|direction|文本方向|
|line-height|行高|
|letter-spacing|字符间距|
|text-align|对齐元素中的文本|
|text-decoration|向文本添加修饰|
|text-indent|缩进元素中文本的首行|
|text-transform|元素中的字母|
|uicode-bidi|设置文本方向|
|white-space|元素中空白的处理方式|
|word-spacing|字间距|


### 案例1 颜色

index.html文件
````
 <head>
        <meta charset="UTF-8">
        <title></title>
        <link rel="stylesheet" href="MyCss.css" type="text/css">
    </head>
    <body>
        <p>查看颜色</p>
        <h1>标题查看颜色</h1>
    </body>
</html>
````
MyCss.css文件
````
body{
  color:aqua;
  }
````

### 案例2：text-align
text-align是一个基本的属性，它会影响一个元素中的文本行互相之间的对齐方式。

值left，right和center会导致元素中的文本分别左对齐、右对齐和居中。默认值是left

Mycss.css文件
 ````
 body{
  color:red;
  text-align:center;
  }
````
 
 ### 案例3： text-indent
 
 缩进文本：把Web页面上的段落的第一行缩进，是一种最常用的文本格式化效果。通过使用text-indent属性，所有元素的第一行都可以缩进一个给定的长度，设置该长度可以是负值。
 
 下面的规则可以是所有段落的首行缩进 5 em：
 
 ````
 p{
    text-indent:5em;
   }
````

index.html文件

````
<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
        <link rel="stylesheet" href="style.css" type="text/css">
    </head>
    <body>
        <div>
            <h3>实验楼</h3>
            <p>做最真实的 IT 学习环境，</p>
            <p>做最真实的 IT 学习环境。</p>
            <p>做最真实的 IT 学习环境，</p>
            <p>做最真实的 IT 学习环境。</p>

        </div>
    </body>
</html>
````
 
 


