### 1. js的声明和引入

##### 1.声明

1.  在head标签中使用script标签进行js代码域的声明

    ```html
    <scprit type="text/javascript">
    	alert("this is my first js.")
    </scprit>
    ```

    ​		作用：声明js代码域

    ​		特点：js的代码只会作用于当前网页

2.  在head标签中使用javascript标签引入外部声明好的js文件

```html
<scprit src="xxx.js" type="text/javascript" charset="utf-8"></scprit>
```

​		作用：引入外部声明好的js文件

​		特点：实现js代码的重复使用，避免代码的冗余。

注意：

​		因为js在html文档中是一门单独的的语言，可以声明在文档中的任意位置

​		一般情况下：声明在head标签中

##### 2. 例子

```html
<!DOCTYPE html>
<html>
    <head>
        <title>js的声明和引入</title>
        <meta charset="utf-8">
        <!--声明js代码域-->
        <script type="text/javascript">
            alert("这是我的第一个js")
        </script>
    </head>
    <body>
        <h3 align="center">js的声明和引入</h3>
    </body>
</html>
```

### 2. js的变量

##### 1.变量只有var类型

```html
        <script type="text/javascript">
            var a=123;
            var a1="js";
            var a2=true;
            var a3=new Date();
            alert(a3);
        </script>
```

注意：js中代码可以不用“；”结束，为了提高可读性，一般使用“；”

##### 2.js的数据类型

-   数据类型判断关键字：typeof

-   数据类型：

    -   number:	所有的数字类型

    -   string:        字符串类型

    -   boolean:    布尔类型

    -   object：     对象类型

    -   null：          空对象赋值，主要是与Undefined区分

        ```js
        var c=null
        ```

    -   Undefined:未赋值的情况，默认值是Undefined

        ```js
        var c;
        alert(typeof c);
        ```

    注意：js中尽可能要给变量赋初始值			

    ​			数据类型影响变量的类型

    ##### 3. 数据类型强制转换

    ```js
    var a=1;
    var b="123";
    alert(typeof Number(b)); 
    alert(typeof Boolean(a));
    ```

### 3. js的运算符

#### 1.基本运算符：

##### 	1.算术运算符

​	加法：+

​	减法：-

​	乘法：*

​	除法：/

​	除余：%

​			number类型和number类型

​			number类型和boolean类型（false--0，true--1）

​			number类型和stirng类型的数字

​			string类型的数字和string类型的数字

​			string类型的数字和boolean类型

​	注意：如果两边不是number数据类型，则会使用Number()函数强制转换，再进行计算。

##### 	2.逻辑运算符（与java中一致）

​	与：&   &&

​	或：|    ||

​	非：！

##### 	3.关系运算符(与java中一致)

##### 	4.自增运算符

​	++    --    -=     +=

#### 2. 特殊运算符:

​            1.等值运算符:==

​                类型一致直接比较

​                类型不一致,先使用Number强转后再进行比较

​            2.等同运算符:===

​                类型不一致直接返回false

​                类型一致,再比较内容,内容一致返回true,不一致返回false.



​            注意:null==undefined的值为:true

​                null===undefined的值为:false

```html
<!DOCTYPE html>
<html>
    <head>
        <title>js的运算符</title>
        <meta charset="utf-8">
        <!--声明js代码域-->
        <script type="text/javascript">
            /*基本运算符和java一致*/

            /*特殊关系运算符*/
            var a1=1;
            var a2="1";
            var a3=true;
            var a4="true";
            var a5="a";
            var a6="a";
            //-----==运算符-----
            alert(a1==a2);//true
            alert(a1==a3);//ture
            alert(a1==a4);//false
            alert(a2==a3);//true
            alert(a2==a4);//false
            alert(a3==a4);//false
            alert(a5==a6);//true

            //-----===运算符-----
            alert(a1==a2);//false
            alert(a1==a3);//talse
            alert(a1==a4);//false
            alert(a2==a3);//false
            alert(a2==a4);//false
            alert(a3==a4);//false
            alert(a5==a6);//true

        </script>
    </head>
    <body>
        <h3 align="center">js的运算符</h3>
    </body>
</html>
```

### 4. js的逻辑结构和循环结构

##### 1.逻辑结构

​            1.if结构

​                    if(){}

​                    if(){}else{}

​            2.switch选择结构

​                    switch(){case...}

##### 2.循环结构

​           1.for(){}

​           2.while(){}

​           3.do{}while()

```html
<!DOCTYPE html>
<html>
    <head>
        <title>js的逻辑结构和循环结构学习</title>
        <meta charset="utf-8">
        <!--声明js代码域-->
        <script type="text/javascript">
            //经典九九乘法表
            for(var i=1;i<10;i++){
                for(var j=1;j<=i;j++){
                    document.write(i+"*"+j+"="+i*j+"&nbsp;&nbsp;&nbsp;&nbsp;");
                }
                document.write("<br>");
            }
        </script>
    </head>
    <body>
        <h3 align="center">js的逻辑结构和逻辑结构</h3>
    </body>
</html>
```

### 5. js的数组

##### 1.数组的声明

​                    var arr=new Array();         第一种声明方式

​                    var arr2=new Array(length);  第二种声明方式

​                    var arr3=[];                 第三种声明方式(最常用)

##### 2.数组的赋值和取值

​                    数组可以存储任何不同类型的数据,长度不固定,不会有脚标溢出问题

##### 3.数组的length属性

​                    var arr=[]

​                    arr.length

​					改变length的值,可以改变数组的长度

##### 4.数组的遍历

​					1.遍历:	for形

```js
//遍历1
            var arr=[1,"213",3,"ad",4];
            for(var i=0;i<arr.length;i++){
                alert(arr[i]);
            }
```

​					2.遍历:	for-in形

```js
 //遍历2
            var arr=[1,"213",3,"ad",4];
            for(var i in arr){
                alert(arr[i]);
            }
```

##### 5. 数组的常用操作：

1.  数组的合并

    ```js
    var d = arr.concat(b,a,a);       //数组的合并
                alert(d);
    ```

2.  数组指定间隔符转换字符串

    ```js
    var b = arr.join("-");         //数组指定间隔符转换字符串
    alert(typeof b);
    alert(b)
    ```

3.  数组移除最后一个元素并返回

    ```js
    var ele = arr.pop();           //移除数组最后一个元素并返回
    alert(ele);
    ```

4.  数组的追加，返回新的长度

    ```js
    var ln = arr.push("lol");      //数组的追加
    var ln2 = arr.push("44","55");
    alert(arr);
    ```

5.  数组移除第一个元素

    ```js
    var ele = arr.shift();         //移除数组的第一个元素，并返回
    alert(ele);
    ```

6.  数组在开始位置插入指定元素

    ```js
    arr.unshift("friday");          //在第一个位置插入元素
     alert(arr);
    ```

7.  数组删除指定位置的元素

```js
arr.splice(1,2);                //删除数组指定位置的元素
alert(arr);
```

### 6. js的函数

##### 1. 函数的声明

方式1(常用)

```js
function test1(a1,a2){
         alert("函数的声明1");
} 
```

方式2

```js
var test2 = new Function("a1","a2","alert('函数声明2')");
```

方式3

```js
var test3=function(a1,a2){
   	 alert("函数声明3");
}
```



##### 2. 函数的参数

```js
 function testParam(a1,a2){
        alert("函数的形参");
}
testParam();     //形参都有默认的值undefined,所以在调用时，形参可以不赋值。
testParam(1);
testParam(1,2);
```

##### 3. 函数的返回值

```js
var testReturn=function(){
       alert("函数的返回值");
       return "javascript";
}
alert(testReturn());
```

​	在js中如果函数有返回值，则直接返回，如果没有，则返回默认的undefined。

##### 4. 函数作为实参

以一个函数名作为另外一个函数的参数进行传递。

### 7. js的类和对象

#### 1. 类：

##### 1、类的声明

```js
function Person(name,age){
                this.name = name;
                this.age = age;
                this.aihao = "running";
                this.test=function(a){
                    alert(a);
                }
}
```

##### 2、类的使用

```js
var p = new Person("John",32);      //创建类的对象
var p1 = new Person("Bob",24);
p.address = "北京";             //可以随意添加对象的属性
alert(p.address);
alert("name = "+p.name+"，"+"age = "+p.age+","+"爱好是"+p.aihao);
```

##### 3、类的“继承”

  使用prototype关键字（它就属于类的属性，与对象无关）

```js
Person.prototype.txt="haha";   //添加属性txt使它成为Persion类的属性
alert(p.txt===p1.txt); //true
```

#### 2. 对象：

##### 1.作用：用来存储整体数据。

##### 2.原因：很多时候我们没有办法预先知道一个对象应该有哪些属性，所以只能临时创建一个对象来自定义属性存储数据，来保证数据的完整性。

##### 3.使用：

```js
//自定义对象(方式1)
            var obj = new Object();
            obj.name = "John";
            obj.age = 19;
            obj.sex = "F";
            obj.test=function(){
                alert("haha");
            }
//方式2
            var obj = {
                this.name = name;
                this.age = age;
                this.aihao = "running";
                this.test=function(a){
                    alert(a);
                }
            }
```

注意：js中的对象属性和内容是可以扩充的，不是依赖于类的声明的，类只是对象公共部分的一种声明，是为了节省代码的冗余。

### 8.js的常用方法和对象

##### 1.String对象：（和java基本一致）

​	1.大小写转换:

```js
var a = "abc";
var b = "ABC";
a.toUpperCase();
b.toLowerCase();
```

​	2.截取字符串：

​	substr(start_index,length)、substring(start_index,end_index)

​	3.查找字符位置

​	indexOf()、lastIndexOf()

##### 2.Date对象：

​	创建如期对象：

```js
var date = new Date();
//获取年份
date.getYear();//获得从1900年开始距今的年份数
date.getFullYear();//获得当前年份
//获取月份
date.getMonth()+1;//获得当前月份
//获取日期
date.getDate();//返回当前日期
//获取星期数
date.getDay();//返回星期数，注意星期日是0
//获取当前时间
date.getHours();
date.getMinutes();
date.getSeconds();
```

​	

##### 3.Math对象：

​	random();

​	round();返回一个按照指定的小数位数进行四舍五入运算的结果

​	ceil();

​	floor();

```js
//100-1000向下取整
alert("随机数："+Math.floor(Math.random()*900+100)); 
```

##### 4.Global对象：

​	eval();

​	isNaN();

​	parseInt();

​	parseFloat();

```js
//eval方法(将字符串转译成js代码)
            eval("var a = '123'");
            alert(a);
//isNaN方法(判断Number强转后是否是数字)
            if(!isNaN(a)){
                alert("是数字");
            }
            else{
                alert("不是数字");
            }
//parseInt返回“123abc”中的123，如果没有123，则返回NaN
            alert(parseInt("12ahdf"));  //返回12
            alert(parseInt("abkfjh"));  //返回NaN
//parseFloat
            alert(parseFloat("1.23fjdks"));
            alert(parseFloat("jkjf"));
```



### 8. js的事件机制

作用：根据用户的行为触发响应的js函数的执行，实现网页和用户之间的互动。

##### 1. 单双击事件

单击：onclick

双击：ondblclick

##### 2. 鼠标事件

鼠标悬停：onmouseover

鼠标移出：onmouseout

鼠标移动：onmousemove

##### 3. 键盘事件

键盘弹起：onkeyup

键盘下压：onkeydown

##### 4. 焦点事件

获取焦点：onfocus

失去焦点：onblur

##### 5. 页面加载事件

onload------body标签

##### 6. 值改变事件

onchange----下拉框标签

##### 注意：

​	1. 在html中直接使用事件属性进行添加，属性值为所监听执行的函数。

​	2. js中的事件只有在当前html页面中有效。

​	3. 一个html元素可以添加多个事件。

​	4. 一个事件可以监听触发多个函数的执行，但是不同的函数要用分号间隔。

​    5. 给html添加多事件时，要注意事件之间的冲突。

​			如：单击和双击（双击事件包含单击事件,发生冲突）

​    6. 事件的阻断

​		当事件所监听的函数将返回值返回给事件时：

​				true：则继续执行当前事件所在的html标签的功能

​				false：则会阻断当前事件所在的html标签的功能

##### 7. 超链接调用js函数

```js
function testHref(){
    	alert("我是超链接调用js函数");
}
```

```html
<a href="javascript:testHref()" >调用js函数</a>
```

### 9.js的window对象

BOM浏览器对象模型：是规范浏览器对js语言的支持(js调用浏览器本身的代码)。

BOM的具体实现是window对象。

##### 1.window的常用方法

1.  window对象不用new，直接使用，window关键字可以省略不写。

2.  框体方法

    ```js
            //警告框（无返回值）
            function testAlert() {
                var al = window.alert("我是警告框");
                alert(al);
            }
    
            //确认框（有返回值）
            function testConfirm() {
                var co = window.confirm("你确定要删除吗？");
                alert(co);
            }
            //提示框（有返回值）
            function testPrompt() {
                var pr = window.prompt("请输入昵称：");
                alert(pr);
            }
    ```

    

3.  定时和间隔执行方法

    ```js
            /*定时执行方法*/
            var idi; //声明全局变量
    
            function testSetTimeout() {
                idi = window.setTimeout(function() {
                    alert("我是定时执行");
                }, 3000);   //时间单位是毫秒
            }
            //停止当前的定时执行
            function testClearTimeout() {
                window.clearTimeout(idi);
            }
    
            //间隔执行方法(每间隔一定时间执行一次)
            var ids; //声明全局变量
    
            function testSetInterval() {
                ids = window.setInterval(function() {
                    alert("我是间隔执行");
                }, 2000);
            }
            //停止当前的间隔执行
            function testClearInterval() {
                window.clearInterval(ids);
            }
    ```

4.  子窗口方法

    window.open('子页面的资源(相对路径)','打开方式','配置');

    示例：

    ```js
     window.open('10-js-son.html', 'newwindow', 'height=400, width=600, top=100, left=300, toolbar=yes, menubar=yes, scrollbars=yes, resizable=yes, location=yes, status=yes');
            
    ```

    

    ```js
            function testTime() {
                window.setInterval(function() {
    
                    var span = document.getElementById("spanTime");
                    span.innerHTML = span.innerHTML - 1;
                    //关闭子页面
                    if (span.innerHTML == 0) {
                        window.close();
                    }
                }, 1000);
            }
    ```

    

5.  子页面调用父页面的函数

window.opener.父页面的函数;

##### 2.window的常用属性

-   地址栏属性

    ```js
    window.location.href="新的地址(URL)或新的资源路径";
    window.location.reload();
    ```

    历史纪录属性

    ```js
    window.history.forward();//历史纪录前进
    
    window.history.back(); //历史纪录后退
    
    window.history.go(index); //跳转到指定的历史纪录
    	//注意：window.history.go(0);   刷新此页面
    ```

-   屏幕属性（了解）

    ```js
    //获得屏幕的分辨率
    
    window.screen.width;
    
    window.screen.height;
    ```

-   浏览器配置属性（不常用）

    ```js
    window.navigator.userAgent; //获得浏览器的配置信息
    ```

    

-   主题面板属性（document）

    

### 10.js的document对象

#### 1、document概念

​		浏览器对外提供的文档js的用来操作HTML文档的一个对象，此对象封存的HTML文档的所有信息。

#### 2、使用document

1.  ##### 获取HTML元素对象

    直接方式

    1.  document.getElementById("")
    2.  document.getElementByName("")
    3.  document.getElementByTarName("")
    4.  document.getElementByClassName("")

    间接方式

    1.  父子方式

        ​     

        ```js
           function testParentsToChilds() { //父子关系
        ​            var id = document.getElementById("parentsdiv");
        ​            var childs = id.childNodes;
        ​            alert(childs.length);  //三个东西四个空，一共是7个
        ​        }
        ```

        

    2.  子父方式

        ​       

        ```js
         function testChildToParents() { //子父关系
        ​            var id = document.getElementById("sondiv1");
        ​            var childs = id.parentNode;
        ​            alert(childs);
        ​        }
        ```

        

    3.  兄弟关系

        ​       

        ```js
        function testBrother() { //兄弟关系
            ​            var bor = document.getElementById("sondiv2");
            ​            var gg = bor.previousElementSibling;
            ​            var dd = bor.nextElementSibling;
            ​            alert(gg + ":" + dd);
            ​        }
        ```

        

2.  ##### 操作HTML元素的属性

    ###### 固定属性

    -   获取属性值

        元素对象名.属性名     // 返回当前属性值

        ```js
        <input type="text" name="" id="uname" value="">
        function test1(){
            //获取元素对象
            var inp=document.getElementById("uname");
            //获取固有属性值
            alert(inp.type);
        }
        ```

    -   修改属性值

        元素对象名.属性名=属性值

        ```js
        <input type="text" name="" id="uname" value="">
        function test1(){
            //获取元素对象
            var inp=document.getElementById("uname");
            //修改固有属性值
            inp.type = "button";
        }
        ```

    注意：尽量的不要去修改元素的id值和name值

    ###### 自定义属性

    -   获取属性值

        元素对象名.getAttribute("自定义属性名")

        ```js
        <input type="text" name="" id="uname" value="" abc="lala">
        function test(){
            //获取元素对象
            var inp=document.getElementById("uname");
            //获取自定义属性值
            inp.getAttribute("abc");
        }
        ```

    -   修改属性值

        元素对象名.setAttribute("自定义属性名","修改后的属性值")

        ```js
        <input type="text" name="" id="uname" value="" abc="lala">
        function test1(){
            //获取元素对象
            var inp=document.getElementById("uname");
            //修改自定义属性值
            inp.setAttribute("abc","haha");
        }
        ```

    注意：使用自定义方式获取固有属性内容，value值获取的是默认值，不能获取用户输入的数据。

3.  ##### 操作HTML元素的内容和样式

    ###### （1）内容：

    -   获取元素内容：

    ​	元素对象名.innerHTML   //返回元素对象的所有内容，不包括HTML标签

    ​	元素对象名.innerText      //返回元素对象的文本内容，包括HTML标签

    -   修改元素内容：

    ​	元素对象名.innerHTML="修改后的内容"  //覆盖元素的原有内容

    ​	元素对象名.innerHTML=元素对象名.innerHTML+"追加的内容" //追加内容

    ​	元素对象名.innerText="修改后的内容"  //覆盖元素的原有内容，但HTML标签不会被解析，会作为普通文本显示。

    ###### （2）样式：

    方式1：（通过style方式）

    -   js给元素添加样式：

        元素对象名.style.添加的样式="添加的样式值"

    -   js给元素修改样式：

        元素对象名.style.修改的样式="修改的样式值"

    -   js给元素删除样式：

        元素对象名.style.删除的样式=""

    方式2：（通过className方式）

    -   添加或修改

        元素对象名.className="<u>新的类选择器</u>  或者  <u>修改类选择器</u>"

    -   删除

        元素对象名.className=""

4.  ##### 操作HTML的文档结构

    -   添加节点

        (1).  div.innerHTML=div.innerHTML+"内容" 

        ```js
                    //添加节点
                    function testAdd(){
                        var files = document.getElementById("showdiv");
                        files.innerHTML=files.innerHTML+"<div><input type='file' id='' name='' value='' ><input type='button' value='删除' onclick='delNode(this)'></div>"
                    }
        ```

        (2).  var 标签对象名=对象名.createElement("标签")

        ​		标签对象名.标签的属性=属性值

        ​		对象名.appendChild(标签对象名)

        ```js
                        //创建文件标签
                        var file=document.createElement("input");
                        file.type="file";
                        //创建按钮标签
                        var bt=document.createElement("input");
                        bt.type="button";
                        bt.value="delete";
        ```

    -   删除节点

        (1).  div.innerHTML=""

        ​		父节点.removeChild(子节点对象)

        ```js
                    //删除节点
                    function delNode(btu){
                        //获得父节点对象
                        var files = document.getElementById("showdiv");
                        //获得子节点对象
                        var cdiv = btu.parentNode;
                        //父节点删除子节点
                        files.removeChild(cdiv);
                    }
        ```

        (2).  对象名.removeChild("标签对象名")

        ```js
                        bt.onclick=function(){
                            inp.removeChild(file);
                            inp.removeChild(bt);
                            inp.removeChild(br);
                        }
        ```

5.  ##### document操作Form元素

    1.  获取form表单对象

        使用id：var fm=document.getElementById("fm");

        使用name：var frm=document.frm;

    2.  获取form下所有表单元素对象的集合

        fm.elements;

    3.  form表单的常用方法

        表单对象.submit();   //提交表单数据

    4.  form的属性操作

        表单对象.action="新的值" //动态改变数据的提交路径

        表单对象.method="新的值"  //动态改变数据的提交方式

    **js的通用属性**

    ​	只读模式：

    ​				readonly="readonly"   //不可以更改，但数据可以提交

    ​	关闭模式：

    ​				disabled="disabled" //不可以进行任何操作

    

6.  ##### document操作表单

    -   js操作多选框、单选框

        被选中状态下在js中checked属性值为true，未被选中状态为false

    -   js操作下拉框

        被选中的option对象在js中selected属性值为true，未被选中状态为false

    

7.  ##### document对象操作表格

    -   删除行

        ```js
                    function testDelTable(btn){
                        //获取表格对象
                        var tab=document.getElementById("ta");
                        //获取表格行对象
                        var tr_index = btn.parentNode.parentNode;
                        //删除表格行元素
                        tab.deleteRow(tr_index.rowIndex);
                    }
        ```

        行对象.rowIndex    //返回行对象的脚标

        表格对象.deleteRow(要删除的行对象脚标)

    -   修改功能

        ```js
        //修改数量(将文本内容改成文本框)
                    function testUpdate(btn){
                        	//获取单元格对象
                        	var tr=btn.parentNode.parentNode;
                        	//获得第四列的单元格对象
                        	var cell=tr.cells[3];
                        	//判断cell.innerHTML的值是否为数字
                        	if(!isNaN(cell.innerHTML)){
                           	 	//修改单元格内容
                            	cell.innerHTML="<input type='text' value='"+cell.innerHTML+"' onblur='testUpdate2(this)'/>";
                        		}
                    }
        //将文本框内容改成文本
                    function testUpdate2(inp){
                        	var cell=inp.parentNode;
                        	cell.innerHTML=inp.value;
                    }
        ```

    -   删除、复制行、添加行、隔行变色(通过for循环实现多行操作)

        删除：tab.deleteRow(tr_index.rowIndex);

        复制：var tr=table.insertRow(行号)

        ​			tr.innerHTML=ta.rows[i].innerHTML

        添加行：var tr=table.insertRow(行号)

        ​			   var cell0=tr.insertCell(列号)；

        ​				cell0.innerHTML="";

        隔行变色：取得隔行的行号，操作颜色样式即可。

