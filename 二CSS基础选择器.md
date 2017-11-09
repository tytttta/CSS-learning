# CSS-基础选择器

## 1.1 派生选择器

通过依据元素在其位置的上下文关系来定义样式，可以使标记更加简洁。

派生选择器允许根据文档的上下文关系来确定某个标签的样式。通过合理的使用派生选择器使HTML代码更简洁。

案例：希望列表中的strong元素变为红色，而不是默认的黑色，可以定义一个派生选择器：

    li{
        color:red;
    }
    
HTML的标记为

    <p><strong>我是黑色，因为我不在列表中</strong></p>
    <ul>
        <li><strong>我是红色，因为strong元素在li元素中</strong></li>
     </ul>
     
## 1.2 id 选择器

### 1 id选择器

id选择器可以为标有id的HTML元素指定特定的样式，id选择器以“#” 来定义

### 2 id选择器和派生选择器

id选择器通常用于建立派生选择器

案例：

MyCss.css文件

    #pid a{
        color:greed;
        }
    
    #divid{
        color:red;
        }
        
 index.html文件：
 
    <p id=pid>Hello css< a href="www.baidu.com">baidu</a></p>
    
    <div id="divid"> this is a div</div>
    
 ## 1.3类选择器
 
 ### 1.3.1 在CSS中，类选择器以一个点号显示
 
    .divclass{
        color:red;
        }
        
 在下面HTML代码中，div元素含有divclass类，意味着他要遵守.divclass的规则。
 
    <div class="divclass">
        hello div
    </div>
    
 注意：类名的第一个字符不能使用数字。
 
 ### 1.3.2 和id一样，class也可被用于派生选择器
 
    .pclass a{
        color:greed;
        }
        
  案例：
  
  MyCSS.css文件
  
    .pclass a{
        color:red;
        }
      
     .divclass{
        color:green;
        }
    
   index.html文件：
    
    <p class="pclass">这是一个class显示效果<a href="www.baidu.com">效果</a></p>
    
    <div class="divclass">hello div</div>
 
## 1.4 属性选择器

对带有指定属性的HTML元素设置样式。

### 1.4.1 下面例子为带有title属性的所有元素设置样式

    <style>
       [title]{color:red;}
    </style>
    
### 1.4.2 属性和值选择器

下面的例子为title=“te”的所有元素设置样式

    <style>
    [title=te]{color=red;}
    </style>
    
 ### 1.4.3 案例
 
 index.html文件
    
    <title></title>
    <style type="text/css">
        [title]{color:red;}
        [title=te]{color=green;}
    </style>
    
    <body>
        <p title=>属性选择器</p>
        <p title="te">属性和值选择器</p>
    </body>
        


