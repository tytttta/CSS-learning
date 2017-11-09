# 一、CSS 指的是层叠样式表（Cascading StyleSheet）
CSS 在网页制作中用来对页面的布局、字体、颜色、背景加以控制。

CSS学习路径
![CSS学习路径图片](https://github.com/tytttta/CSS-learning/blob/master/pic.jpg);

# 二、CSS 基础语法规则
## 2.1 CSS规则有两个主要的部分构成：选择器，以及一条或多条声明。
selector{
   declaration1;
   declaration2;
   declaration3;
}

选择器通常是需要改变样式的HTML元素。每条声明由一个属性和一个值组成，属性和值之间冒号分开。
selector{property:value}
例：
h1{
   color:red;
   font-size:14px;
   }
   
注意：如果值大于一个单词，则需要加引号:
p{font-family:"sans serif"}

## 2.2 案例分析：

index.html 文件

  <html>
      <head>
          <meta charset="UTF-8">
          <title></title>
          <!--引外部资源 MyCss.css-->
          <link rel="stylesheet" href="MyCss.css" type="text/css">
      </head>
      <body>
          <h1>
              shiyanlou
          </h1>
      </body>
  </html>
  
  MyCss.css  文件
  
  h1{
    color: red;font-size: 50px;
}

## 2.3 CSS高级语法
### 2.3.1 选择器的分组
可以对选择器进行分组，这样被分组的选择器就可以分享相同的声明。用逗号将需要分组的选择器分开。
h1,h2,h3{
  color:red;
  }
  
### 2.3.2 继承
 
 子元素从父元素继承属性
 
 body{
        color:greed;
        }
 通过CSS继承，子元素将继承最高级元素所拥有的属性（这些子元素如p,td,ul,ol,li,dl,dt和dd）。所有的body的子元素都显示为绿色，子元素的子元素也一样。
 
 案例：
 
 index.html文件
 
  <html>
    <head>
        <meta charset="UTF-8">
        <title></title>
        <link rel="stylesheet" href="mycss.css" type="text/css">
    </head>
    <body>
        <h1>
            shiyanlou
        </h1>
        <a>love</a>
        <h2>h2</h2>
        <h3>h3</h3>
        <h4>h4</h4>
    </body>
</html>

MyCSS.css文件

   h1,a,h2{
    color: red;font-size: 50px;
        }
        body{color: blue;}
        h4{
           color:green;
        }
 在CSS代码中定义了h1,a,h2,h4的颜色，没有定义h3,考虑继承，h3的颜色为body定义的颜色。  
  
 
 
 
 
 
