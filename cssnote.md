### 1. CSS简介

-   作用:	1.专门给网页进行样式开发.	2.给网页进行布局

-   特点:	1.语言特别简单.	2.开发的样式可以重复使用
-   使用: 
    -   css的声明
    -   css的选择器
    -   css的常用样式
    -   css的盒子模型
    -   css的定位
    -   css的布局

### 2. css的声明

##### 1.声明:

-   位置:	在头标签(head)中使用style标签声明

    作用:	公共样式或某个标签的单独样式

    ```css
            <style type="text/css">
                hr{
                    width: 50%;
                    height: 20px;
                    color: red;
                    background-color: red;
                }
            </style>
    ```

    

-   位置:    在标签上使用style属性进行声明

    作用:    直接作用于当前标签

    ```css
    <hr style="background-color:blue;height:50px"/>
    ```

    

-   位置:    在head标签中使用link标签引入声明好的css文件

    作用:    此声明相当于调用

    ```css
    hr{
        width:50%;
        height:20px;
        color:gray;
        background-color:gray;
    }
    ```

    

    ```css
    <link rel="stylesheet" type="text/css" href="css声明.css">
    ```

    

##### 2.注意:

如果css的声明全都在head中,则遵循就近原则,谁离标签近,就会被显示

### 3. css的选择器

#####  1.css选择器:

​                标签选择器

​                    标签名{样式1:样式1值;...}

​                    作用:给当前网页中所有的该标签增加相同的样式

​                id选择器

​                    \#标签的id{样式1:样式1值;...}

​                    作用:给某个指定的标签增加指定的样式

​                类选择器

​                    .类选择器名{样式1:样式1值;...}

​                    作用:给不同的标签添加相同的样式

​                全部选择器

​                    *{样式1:样式1值;...}

​                    作用:选择所有的HTML标签,并添加相同的样式

\-------------------------------------------------------------------------

​                组合选择器

​                    选择器1,选择器2,...{样式1:样式1值;...}

​                    作用:解决不同选择器之间重复样式的问题

​                子标签选择器

​                    选择器1 子标签选择器{样式1:样式1值;...}

​                    作用:解决子标签样式问题

​                属性选择器

​                    标签名[属性名=属性值]{样式1:样式1值;...}

​                    作用:选择某标签具备某属性并且属性值为某属性值的标签的样式

##### 2.css的使用过程:

​		1.声明css代码块

​		2.使用选择器选择要添加样式的标签

​		3.书写样式单

##### 3.例子

```html
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <meta charset="utf-8">

        <!--声明css代码域-->
        <style type="text/css">
        /* 标签选择器 */
            table{
                width:300px;
                height:200px;
                border:solid 1px;
            }

        /* id选择器 */
        #t1{
            background-color:red;
        }
        /* 类选择器 */
        .commen{
            color:yellow;
        }
        /* 全部选择器*/
        *{

        }
        /*组合标签选择器*/
        .commen,table{
            color:blue;
        }
        /*子标签选择器*/
        ul li a{
            color:black;
        }
        #p1 a{
            color:yellow
        }

        /*属性选择器*/
        input[type="password"]{
            background-color: red;
        }
        </style>
    </head>
    <body>
        <h3 align="center">css的选择器学习</h3>
        <hr />
        <hr class="commen"/>
        <table id=t1 >
            <tr>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td></td>
                <td></td>
            </tr>
        </table>
        <table class="commen">
            <tr>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td></td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td></td>
                <td></td>
            </tr>
        </table>
        <ul>
            <li><a href="">哈哈</a></li>
            <li><a href="">嘿嘿</a></li>
            <li><a href="">呵呵</a></li>
        </ul>

        <p id="p1">
            <a href="">嘻嘻</a>
        </p>
        <p>
            <a href="">ha嘻</a>
        </p>
        
        <input type="text" name="t" id="" value="">
        <input type="password" name="" id="" value="">
    </body>
</html>

```



### 4. css的常用样式

##### 1.边框设置

```css
border:solid 1px;
```

##### 2.字体设置

font-size:10px;

font-family:"黑体";

font-weight:bold;设置字体加黑

##### 3.字体颜色设置

color:颜色;

##### 4.背景颜色设置

background-color:颜色;

##### 5.背景图片设置

background-img:url(图片路径);

background-repeat:no-repeat;图片不重复

background-size:cover; 图片平铺整个页面

##### 6.宽高设置

##### 7.浮动设置

float:left/right

##### 8.行高设置

line-height:10

### 5. css的盒子模型

##### 1.div(分割)标签:

​		块级标签,主要是用来进行网页布局的,会将其中的子元素内容作为一个独立的整体存在.

​		特点:

​				1.默认宽度是页面的宽度,但是可以设置

​				2.高度默认是没有的,但是可以设置

​				3.如果子元素设置了百分比的高或者宽,占据的是div的百分比,不是页面的.

##### 2.盒子模型:

外边距:margin

​		作用:用来设置元素与元素之间的间隔

​		居中设置:margin: 0px auto;上下间隔为0,水平居中.

​		可以根据需要单独设置上下左右的外边距.

边框: border

​		作用: 用来设置元素之间的边框大小

​			可以单独设置上下左右边框

内边框:  padding

​		作用: 用来设置内容与边框的距离

​		注意: 内边距不会改变内容区域的大小

​		可以单独设置上下左右内边距

内容区域:

##### 3.例子

```html
<!DOCTYPE html>
<html>
    <head>
        <title>css盒子模型的学习</title>
        <meta charset="utf-8">
        <style type="text/css">
            #div01{
                border:solid 5px;
                width:200px;
                margin-left:20px;
                margin:0px auto; /*上下间隔是0px,水平居中*/
                padding:20px;   /*内容与边框的间距*/
            }
            #div02{
                width:200px;
                border:dashed 30px;
                margin-bottom: 10px;
                margin-left:20px;
                margin:10px auto;
                padding: 20px;
            }

        </style>

    </head>
    <body>

        <div id="div01">
            <h3 align="center">this is a div</h3>
        </div>

        <div id="div02">
            <h3 align="center">this is a div</h3>
        </div>
    </body>
</html>
```



### 6. css的定位

(position)

##### 1.相对定位:

relative

​		作用:相对元素原有位置移动指定的距离(相对于自己原有的位置)

​				可以使用top,bottom,left,right移动

​				其它元素不改变位置

##### 2.绝对定位:

absolute

​		作用:参照父元素位置移动指定的距离	

​				可以使用top,bottom,left,right移动

​		注意:如果父级元素成为参照元素,则必须使用相对定位属性	

##### 3.固定定位:

fixed

​		作用:固定在某一位置,不会随着滚动条的滚动而移动位置

​				可以使用top,bottom,left,right移动

##### 4.例子

```html
<htlm>
    <head>
        <title>css定位学习</title>
        <meta charset="utf-8">
        <style type="text/css">

            #div1{
                border:solid 1px black;
                width: 300px;
                height: 200px;
                margin:10px;
                position:relative;
            }
            #div11{
                border:solid 1px black;
                width: 30px;
                height: 20px;
                margin:10px;
                position: absolute;
                top:100px;
            }
            #div2{
                border:dashed 1px black;
                width: 300px;
                height: 200px;
                margin:10px;
                background-color: blue;
                position: relative;
                bottom:-30px;
            }
            #div3{
                border:solid 1px black;
                width: 300px;
                height: 200px;
            }
            #div4{
                border:solid 1px black;
                background-color: red;
                width: 30px;
                height: 30px;
                position:fixed;
                right:20px;
                top:200px;
            }

        </style>

    </head>
    <body>

                <div id="div1">
                    <div id="div11"></div>

                </div>
                <div id="div2">

                </div>

                <div id="div3">

                </div>
                <div id="div4">

                </div>
                <br><br><br><br><br><br><br><br><br><br><br><br><br>
    </body>
</htlm>
```



