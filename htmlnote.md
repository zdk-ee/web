### 1. html-标准文档结构

##### 1. html

```html
<html></html>
```

##### 2.head

```html
<head></head>
```

##### 3.body

```html
<body></body>
```

##### 4.例子

```html
<html>
    <head>
        <!--
			主要是配置 浏览器显示数据的配置信息
				eg: 字符编码等
				一般是给浏览器使用
		-->
    </head>
    <body>
        <!--一般是给用户进行数据显示-->
        this is my fist html.
    </body>
</html>

<!--双标签:<标签名></标签名>
	   单标签:<标签名 />
-->
```

### 2. html-头标签(head)

##### 1. 网页标题

##### 2. 网页标签字符编码

- ```html
  <meta charset="utf-8"/>
  <meta http-equiv="content-type" content="text/html;charset=utf-8">
  ```

##### 3. 关键字

##### 4. 网页描述（了解）

##### 5. 作者（了解）

##### 6. 自动跳转（了解）

##### 7. 例子

```html
<html>
    <head>
        <title>html study你好</title><!--告诉浏览器网页标题-->
        <meta charset="utf-8"/>(html 5格式)<!--告诉网页标题的字符编码格式-->
        <!--<meta http-equiv="content-type" content="text/html;charset=utf-8"/>(html 4格式)-->
        
        <!--
				了解:
						关键字:       keywords
						网页描述:  description
						作者:           author
				作用:
						提高网页在浏览器中的搜索概率.
		-->
        <meta name="keywords" content="HTML ,SXT,小张,509"/><!--网页关键字-->
        <meta name="description" content="本网页是关于学习html,web"/><!--网页描述-->
        <meta name="author" content="小张"/><!--网页作者-->
        
        <meta http-equiv="refresh" content="3;url=http://www.baidu.com"/><!--此网页自动跳转到另一个网页(间隔是3秒)-->
    </head>
    <body>

    </body>
</html>
```



### 3. html-主体标签(body)

#### 1. 文本标签

##### （1）. 标题标签

h1--h6:会将其中的数据加粗显示，并且依次减弱，标题自带换行功能。

​	属性：

​			align：center  left  right

##### （2）. 水平线标签

```html
<hr/>
```

像素单位占的是电脑屏幕的大小，百分比占的是浏览器窗口的大小。

属性：(默认是居中显示)

​			width="宽度"   设置水平线的宽度

​			size="高度"      设置水平线的高度

​			color="颜色"    设置水平线的颜色

​			align="位置"

##### （3）. 段落标签 

```html
<p> <p/>
```

p：将一段数据作为整体进行显示，主要是进行css和js操作时比较方便，会自动换行（段距离大）

##### （4）. 换行符

```html
<br/>
```

br：告诉浏览器此处需要换行（行距小）

##### （5）. 空格符

```html
&nbsp;
<!--代表一个字节-->
```

##### （6）. 权重标签

```html
<b></b>
<!--将内容加黑显示-->

<i></i>
<!--将内容斜体-->

<u></u>
<!--将内容增加下划线-->

<del></del>
<!--将内容增加中划线-->
```



##### （7）例子

```html
<html>
    <head>
        <title>body标签学习</title>
        <meta charset="utf-8"/>
    </head>
    <body>
        <!--标题标签（只有六种方式，字体以次变小，并且有自动换行功能）-->
        <h1 align="center">天气真好</h1>
        <h2>天气真好</h2>
        <h3>天气真好</h3>
        <h4>天气真好</h4>
        <h5>天气真好</h5>
        <h6>天气真好</h6>
        <hr/>  <!--显示一条水平线-->
        <hr width="600px" size="20px" color="red" align="left"/>  <!--显示一条水平线-->
        <p><!--段落-->
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<!--空格-->在联合国成立75周年之际，
            在各国致力于抗击新冠肺炎疫情、推动经济高质量复苏这一特殊时刻，<br><!--换行-->>
            联合国举办<b>生物多样性峰会</b>，<!--将内容加黑-->
            大家共同探讨保护生物多样性、促进可持续发展的重大课题，
            具有现实而深远的意义。---<i>2020.10.2</i><!--将内容斜体-->
        </p>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在联合国成立75周年之际，
            在各国致力于<u>抗击新冠肺炎疫情、推动经济高质量复苏</u><!--将内容增加下划线-->这一特殊时刻，<br>
            联合国举办生物多样性峰会<del>helloworld</del><!--将内容增加删除线-->，
            大家共同探讨保护生物多样性、促进可持续发展的重大课题，
            具有现实而深远的意义。
        </p>
        
        
    </body>
</html>
```



#### 2. 列表标签

##### （1）有序列表

```html
       <!--有序列表-->
        <ol type="i">  <!--type:改变顺序编码的值（1,a,A,i,I）-->
            <li>写代码</li>
            <li>跑跑步</li>
            <li>打游戏</li>
        </ol>
```



##### （2）无序列表

```html
<h3>中国城市</h3>
<ul>
    <li>北京</li>
    <li>上海</li>
    <li>重庆</li>
</ul>
<!--一个li标签中代表一个列表中的一条数据-->
```



##### （3）自定义列表

```html
        <!--自定义列表-->
        <dl>
            <dt>IT课程</dt><!--数据的标题-->
                <dd>java</dd>
                <dd>python</dd><!--数据内容-->
                <dd>大数据</dd>
            <dt>公共基础课程</dt>
                <dd>高数</dd>
                <dd>英语</dd> 
                <dd>体育</dd>
        </dl>
```

##### （4）例子

```html
<html>
    <head>
        <title>列表标签的学习</title>
        <meta charset="utf-8">
    </head>
    <body>
        <h3>中国城市:</h3>
        <!--无序列表-->
        <ul>
            <li>北京</li>
            <li>上海</li>
            <li>重庆</li>
        </ul>
        
        <h3>我的爱好:</h3>
        <!--有序列表-->
        <ol type="i">  <!--type:改变顺序编码的值（1,a,A,i,I）-->
            <li>写代码</li>
            <li>跑跑步</li>
            <li>打游戏</li>
        </ol>
        
        <h3>学校课程:</h3>
        <!--自定义列表-->
        <dl>
            <dt>IT课程</dt><!--数据的标题-->
                <dd>java</dd>
                <dd>python</dd><!--数据内容-->
                <dd>大数据</dd>
            <dt>公共基础课程</dt>
                <dd>高数</dd>
                <dd>英语</dd>
                <dd>体育</dd>
        </dl>
    </body>

</html>

```



### 4. html-图片标签

```html
        <!--图片标签 img -->
        <img src="img/a01.jpg" height="100px"/>
        <img src="img/a02.jpg" height="100px"/>
        <img src="img/a03.jpg" height="100px"/>
```



##### 1. src路径:

​			本地资源路径: 一般用相对路径

​			 网络资源路径: 图片资源的URL地址

##### 2. width:    

设置图片的宽度

##### 3. height:   

设置图片的高度

##### 4. title:        

图片标题,鼠标放在图片上的时候会显示

##### 5. alt:		  

图片加载失败后的提示语

```html
<html>
    <head>
        <title>html的图片标签学习</title>
        <meta charset="utf-8"/>
    </head>
    <body>
        <h3>图片</h3>
        <hr width="500px" size="3px" color="blank" align="left"/>

        <!--图片标签 img "本地资源"和"网络资源"-->
        <img src="img/a01.jpg" height="100px"/>
        <img src="img/a02.jpg" height="100px"/>
        <img src="img/b03.gif" height="100px" title="beautiful" alt="beautiful"/>

        <!--使用网络资源-->
        <img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1601703902321&di=d5497639a230020f85d20ea62ebb97c3&imgtype=0&src=http%3A%2F%2Fa2.att.hudong.com%2F36%2F48%2F19300001357258133412489354717.jpg">
    </body>
</html>
```



### 5. html-超链接标签

##### 1.格式

```html
<a></a>
```

##### 2.属性

href:     要跳转的网页资源路径

​		本地资源:	html文件的相对路径

​		网络资源:	网络资源(网页)的URL

target:	指明要要跳转网页的显示位置

​		_self		在当前页面中刷新

​		_blank	在新的标签页中刷新

​		_top		在顶层页面中刷新

​		_parent  在父级页面中显示

##### 3.锚点

1.使用超链接标签在指定的位置增加锚点,格式:

```html
<a name="锚点名"></a>
```

2.使用a标签可以跳转到指定的锚点位置(在网页内部跳转),格式:

```html
<a href="#锚点名">访问方式</a>
```

3.例子

```html
<html>
    <head>
        <title>锚点学习</title>
        <meta charset="utf-8"/>

    </head>
    <body>
        <h4 align="center">斗罗大陆</h4>
        
        <a href="#first">第一章</a><br>
        <a href="#second">第二章</a><br>
        <a href="#third">第三章</a><br>
        <a href="#fourth">第四章</a><br>
        
        <a name="first"></a>
        <h5>第一章</h5>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;巴蜀，历来有天府之国的美誉，其中，最有名的门派莫过于唐门。
        　　唐门所在是一个神秘的地方，许多人只知道，那是一个半山腰，而唐门所在这座山的山顶有一个令人胆颤心惊的名字，——鬼见愁。
        　　从鬼见愁悬崖上扔出一块石头，要足足数上十九下才会听到石落山底的回声，可见其高，也正是因为这十九秒，尚超过十八层地狱一筹，故而得名。
        　　一名身穿灰衣的青年正站在鬼见愁顶峰，凛冽的山风不能令他的身体有丝毫移动，从他胸口处那斗大的唐字就可以认出，他来自唐门，灰衣代表的，是唐门外门弟子。
        　　他今年二十九岁，因出生不久就进入唐门，在外门弟子的辈分中排名第三，因此外门弟子称他一声三少。当然，到了内门弟子口中，就变成了唐三。
        　　唐门从建立时开始就分为内外两门，外门都是外姓或被授予唐姓的弟子，而内门，则是唐门直系所属，家族传承。
        </p>
        <p>
               &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;此时，唐三脸上的表情很丰富，时而笑，时而哭，但无论如何，都无法掩盖他的那发自内心的兴奋。
            　　二十九年了，自从二十九年前他被外门长老唐蓝太爷在襁褓时就捡回唐门时开始，唐门就是他的家，而唐门的暗器就是他的一切。
            　　突然，唐三脸色骤然一变，但很快又释然了，有些苦涩的自言自语道：“该来的终究还是来了。”
        </p>
        <p>
            　　&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;十七道身影，十七道白色的身影，宛如星丸跳跃一般从山腰处朝山顶方向而来，这十七道身影的主人，年纪最小的也超过了五旬，一个个神色凝重，他们身穿的白袍代表的是内门，而胸前那金色的唐字则是唐门长老的象征。
            　　唐门内门长老堂包括掌门唐大先生在内，一共有十七位长老，此时登山的，也正是十七位。就算是武林大会也不可能惊动唐门全部长老同时出动，要知道，这唐门长老之中，年纪最大的已经超过了两个甲子。
            　　这些唐门长老的修为，无一不是已臻化境，只是转眼的工夫，他们就已经来到了山顶。
        </p>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            　　外门弟子见到内门长老，只有跪倒迎接的份，但此时，唐三却没有动，他只是静静的看着这些脸色凝重的长老来到自己面前，挡住了所有的去路，而在他背后，是鬼见愁。
            　　放下三朵佛怒唐莲，唐三投下最后那恋恋不舍的一眼，嘴角处流露出一丝欣慰的微笑，他毕竟成功了，努力了二十年，他终于完成了这唐家外门暗器的巅峰之作，那种满足的成就，是无法用言语来形容的。
            　　此时此刻，唐三觉得对自己来说，一切都已经不重要了，违背门规也好，生死存亡也罢，似乎都随着眼前这三朵盛开的唐莲而告一段落，佛怒唐莲，这世间最霸道的暗器诞生在自己手中，还有什么比令这浸淫在暗器上一生的唐三更加兴奋的呢？
        </p>

         <a name="second"></a>       
        <h5>第二章</h5>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;老杰克对唐三显然很有耐心，在他心中，村里最懂事的孩子就莫过于眼前的唐三了，真难想象，那样一个父亲怎么会有这么一个乖巧的儿子。
        </p>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“大魂师是魂师级别的称号。魂师是我们整个斗罗大陆中最高贵的职业，他们可以是强大的战士，也可以拥有出色的辅助能力。但不论是哪一种魂师，级别都是按照同样的称号进行排序的。”

        </p>
        <P>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“魂师都拥有自己的武魂力，根据武魂力的强弱，一共分为十大称号。每一个称号又分为十级。最初刚刚入门的，叫做魂士，只要武魂觉醒之后，每个人都是魂士。如果武魂能够修炼的话，当魂力达到十一级的时候，就会进入下一个称号，也就是魂师。而大魂师，就是整个称号序列中的第三个。达到了大魂师境界，就已经是一名相当强大的魂师了。总体的十个称号是这样的。”
　　“魂士，魂师，大魂师，魂尊，魂宗，魂王，魂帝，魂圣，魂斗罗和封号斗罗。我们斗罗大陆的名字，就是由此而来。传说中，达到九十级以上的封号斗罗都可以自行给自己取一个封号，他们简直就是无敌的存在啊！”
        </P>

        <a name="third"></a>      
        <h5>第三章</h5>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;巴蜀，历来有天府之国的美誉，其中，最有名的门派莫过于唐门。
        　　唐门所在是一个神秘的地方，许多人只知道，那是一个半山腰，而唐门所在这座山的山顶有一个令人胆颤心惊的名字，——鬼见愁。
        　　从鬼见愁悬崖上扔出一块石头，要足足数上十九下才会听到石落山底的回声，可见其高，也正是因为这十九秒，尚超过十八层地狱一筹，故而得名。
        　　一名身穿灰衣的青年正站在鬼见愁顶峰，凛冽的山风不能令他的身体有丝毫移动，从他胸口处那斗大的唐字就可以认出，他来自唐门，灰衣代表的，是唐门外门弟子。
        　　他今年二十九岁，因出生不久就进入唐门，在外门弟子的辈分中排名第三，因此外门弟子称他一声三少。当然，到了内门弟子口中，就变成了唐三。
        　　唐门从建立时开始就分为内外两门，外门都是外姓或被授予唐姓的弟子，而内门，则是唐门直系所属，家族传承。
        </p>
        <p>
               &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;此时，唐三脸上的表情很丰富，时而笑，时而哭，但无论如何，都无法掩盖他的那发自内心的兴奋。
            　　二十九年了，自从二十九年前他被外门长老唐蓝太爷在襁褓时就捡回唐门时开始，唐门就是他的家，而唐门的暗器就是他的一切。
            　　突然，唐三脸色骤然一变，但很快又释然了，有些苦涩的自言自语道：“该来的终究还是来了。”
        </p>
        <p>
            　　&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;十七道身影，十七道白色的身影，宛如星丸跳跃一般从山腰处朝山顶方向而来，这十七道身影的主人，年纪最小的也超过了五旬，一个个神色凝重，他们身穿的白袍代表的是内门，而胸前那金色的唐字则是唐门长老的象征。
            　　唐门内门长老堂包括掌门唐大先生在内，一共有十七位长老，此时登山的，也正是十七位。就算是武林大会也不可能惊动唐门全部长老同时出动，要知道，这唐门长老之中，年纪最大的已经超过了两个甲子。
            　　这些唐门长老的修为，无一不是已臻化境，只是转眼的工夫，他们就已经来到了山顶。
        </p>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            　　外门弟子见到内门长老，只有跪倒迎接的份，但此时，唐三却没有动，他只是静静的看着这些脸色凝重的长老来到自己面前，挡住了所有的去路，而在他背后，是鬼见愁。
            　　放下三朵佛怒唐莲，唐三投下最后那恋恋不舍的一眼，嘴角处流露出一丝欣慰的微笑，他毕竟成功了，努力了二十年，他终于完成了这唐家外门暗器的巅峰之作，那种满足的成就，是无法用言语来形容的。
            　　此时此刻，唐三觉得对自己来说，一切都已经不重要了，违背门规也好，生死存亡也罢，似乎都随着眼前这三朵盛开的唐莲而告一段落，佛怒唐莲，这世间最霸道的暗器诞生在自己手中，还有什么比令这浸淫在暗器上一生的唐三更加兴奋的呢？
        </p>

        <a name="fourth"></a>        
        <h5>第四章</h5>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;老杰克对唐三显然很有耐心，在他心中，村里最懂事的孩子就莫过于眼前的唐三了，真难想象，那样一个父亲怎么会有这么一个乖巧的儿子。
        </p>
        <p>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“大魂师是魂师级别的称号。魂师是我们整个斗罗大陆中最高贵的职业，他们可以是强大的战士，也可以拥有出色的辅助能力。但不论是哪一种魂师，级别都是按照同样的称号进行排序的。”

        </p>
        <P>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;“魂师都拥有自己的武魂力，根据武魂力的强弱，一共分为十大称号。每一个称号又分为十级。最初刚刚入门的，叫做魂士，只要武魂觉醒之后，每个人都是魂士。如果武魂能够修炼的话，当魂力达到十一级的时候，就会进入下一个称号，也就是魂师。而大魂师，就是整个称号序列中的第三个。达到了大魂师境界，就已经是一名相当强大的魂师了。总体的十个称号是这样的。”
　　“魂士，魂师，大魂师，魂尊，魂宗，魂王，魂帝，魂圣，魂斗罗和封号斗罗。我们斗罗大陆的名字，就是由此而来。传说中，达到九十级以上的封号斗罗都可以自行给自己取一个封号，他们简直就是无敌的存在啊！”
        </P>
        <a href="#">回到到顶部</a>
    </body>
</html>
```



### 6. html-表格标签

```html
<table>
    ....
</table>
```

##### 1.表格标签:

tr:表示声明一行

​		th:表示声明一个单元格,表头格,数据默认居中加黑显示

​		td:表示声明一个单元格,数据默认居左显示

属性:

​		border:		设置边框

​		width:	   	设置单元格的宽度

​		height:	  	设置单元格的高度

​		cellspacing:  设置边框的大小

​		cellpadding: 设置内容距边框的距离

##### 2. 单元格的合并

行合并:rowspan="合并单元格个数",删除要合并的其他单元格

列合并:colspan="合并单元格个数",删除要合并的其他单元格



注意:如果是田字格合并,则需要两两合并

##### 3. 例子

```html
<html>
    <head>
        <title>html的表格标签学习</title>
        <meta charset="utf-8"/>
    </head>
    <body>
        <h3></h3表格>
        <hr width="500px" size="3px" color="blank" align="left"/>

        <!--
            表格标签学习:
                tr:表示声明一行
                    th:表示声明一个单元格,表头格,默认居中加黑显示
                    td:表示声明一个单元格,默认居左显示
            属性:
                border:显示边框
                width: 设置表格的宽度
                height:设置表格的高度
                cellpadding:设置内容距边框的距离
                cellspacing:设置边框的大小

            合并单元格(表格是规整的):
                行合并:rowspan="合并单元格个数",之后删除要合并的其他单元格
                列合并:colspan="合并单元格个数",之后删除要合并的其他单元格列合并

                注意:如果是四个田字格合并,则两两合并


        -->
            
        <table border="1px" cellpadding="10px" cellspacing="0px">
            <tr height="50px">
                <th width="70px">姓名</th>
                <th width="70px">年龄</th>
                <th width="70px">专业</th>
            </tr>
            <tr height="50px" >
                <td>bryan</td>
                <td>18</td>
                <td>大数据</td>
            </tr>
            <tr height="50px" >
                <td>John</td>
                <td>20</td>
                <td>软件工程</td>
            </tr>

        </table>

        <h3>单元格的合并学习</h3>
        <hr />
        <table border="1px" cellspacing="0">
            <tr height="30px">
                <th width="50px"></th>
                <th width="50px"></th>
                <th width="100px" colspan="2" rowspan="2"></th>
            </tr>

            <tr height="30px">
                <td colspan="2"></td>
            </tr>
            <tr height="30px">
                <td></td>
                <td></td>
                <td rowspan="2"></td>
                <td></td>
            </tr>
            <tr height="30px">
                <td></td>
                <td></td>
                <td></td>
            </tr>
        </table>
    </body>
</html>
```



### 7. html-内嵌和框架标签

##### 1. 内嵌标签

```html
<iframe src="" width="" height="" name=""></iframe>
```

src:	网页资源路径:可以是本地资源,也可以是网络资源(URL)

width: 设置内嵌区域的宽度

height: 设置内嵌区域的高度

name: 设置内嵌区域的名字,结合target使用

```html
<html>
    <head>
        <title>html内嵌标签学习</title>
        <meta charset="utf-8">
    </head>
    <body>
        <a href="https://www.baidu.com" target="_bd">百度一下</a><br>
        <a href="https://www.so.com" target="_so">360搜索</a><br>
        <iframe src="" width="45%" height="400px" name="_bd"></iframe>
        <iframe src="" width="45%" height="400px" name="_so"></iframe>
    </body>
</html>
```



##### 2.框架标签

注意:首先要删除body

​        html框架学习:

​            frameset

​                rows:按照行进行分割页面

​                cols:按照列进行分割页面

​            子标签:

​                frame:进行区域占位,加载一个单独的网页资源

​                    src:资源路径

​                    name:区域名,结合target使用



```html
<html>
    <head>
        <title>html框架学习</title>
        <meta charset="utf-8">
    </head>
    <frameset rows="20%,*,10%">
        <frame src="frame/top.html"/>
        <frameset cols="20%,*">
            <frame src="frame/left.html"/>
            <frame src="frame/right.html"/>
        </frameset>
        <frame src="frame/bottom.html"/>
    </frameset>
</html>
```



### 8. html-表单

##### 1.form表单标签:

​                作用:收集并提交用户数据给指定服务器

​                注意:form标签会收集其标签内部的数据

​                属性:

​                    action:收集的数据提交地址(URL)

​                    method:收集的数据的提交方式

​                        get:适合小量数据,表单数据以?隔开,拼接在URL后面,不同的键值对使用&符号隔开,不安全

​                        post:适合大量数据,安全,隐示提交

##### 2.form表单域标签学习

​        作用:给用户提供可以进行数据书写或者选择的标签

​        使用:

- 文本框:

​                input(type)

​                text 收集少量文本数据,可见

​                password 收集密码数据,不可见

​                name 键

- 单选框:

​                input(type)

​                radio 单选

​                name  属性值相同只能数据选择一个

​                value 要提交的数据

​                checked:checked 使用此属性是默认是选择此项

- 多选框:

​				input(type)

​					 checkbox 多选

​					name  一个多选组name属性值相同

​					value  要提交的数据

​					checked :checked 使用此属性的多选框默认是选择状态

- 下拉框:

```html
<select name="">

	<option value=""></option>

	<option value=""></option>

	<option value=""></option>

</select>
```

​				value 是要提交的数据

​				selected 是默认的选择项

- 文本域:

```html
    <textarea name="" rows="" cols=""></textarea>
```

- 普通按钮:

```html
<input type="button" name="" value="普通按钮">
```



- 隐藏标签:

```html
<input type="hidden" name="" value="">
```



##### 3. form表单标签的使用

​                在点击提交时,form标签会将其内部所有form表单域

​                中用户输入的数据按照method方法提交给action所指的提交地址

##### 4.例子

```html
<html>
    <head>
        <title>表单标签的学习</title>
        <meta charset="utf-8">
    </head>
    <body>
        <h4>form表单标签</h4>
        <hr />
        <!--
            form表单标签:
                作用:收集并提交用户数据给指定服务器
                注意:form标签会收集其标签内部的数据
                属性:
                    action:收集的数据提交地址(URL)
                    method:收集的数据的提交方式
                        get:适合小量数据,表单数据以?隔开,拼接在URL后面,不同的键值对使用&符号隔开,不安全
                        post:适合大量数据,安全,隐示提交
            form表单域标签学习
                作用:给用户提供可以进行数据书写或者选择的标签
                使用:
                    文本框:
                        input
                            type
                                text 收集少量文本数据,可见
                                password 收集密码数据,不可见
                                name 键
                    单选框:
                        input
                            type
                                radio 单选
                                name  属性值相同只能数据选择一个
                                value 要提交的数据
                                checked:checked 使用此属性是默认是选择此项
                    ​多选框:
                    input(type)
                        checkbox 多选
                        name  一个多选组name属性值相同
                        value  要提交的数据
                        checked :checked 使用此属性的多选框默认是选择状态
                    下拉框:
                        <select name="">
                            <option value=""></option>
                            <option value=""></option>
                            <option value=""></option>
                        </select>
                        value 是要提交的数据
                    文本域:
                        <textarea name="" rows="" cols=""></textarea>

                    普通按钮:
                        input (type)
                            button
                        name
                        value
                    隐藏标签:
                        input(type)
                            hidden
                        name
                        value


            form表单标签的使用
                        在点击提交时,form标签会将其内部所有form表单域
                        中用户输入的数据按照method方法提交给action所指的提交地址
        -->
        <form action="#" method="get">
            user_name:&nbsp;&nbsp;&nbsp;&nbsp;<input type="text" name="uname"><br>
            user_psword:<input type="password" name="psword"><br>
            sex: 男<input type="radio" name="sex" value="1" checked="checked"> 女<input type="radio" name="sex" value="0">
            爱好:<br>
            吃饭:<input type="checkbox" name=aihao value="1" checked="checked">
            睡觉:<input type="checkbox" name=aihao value="2" >
            打豆:<input type="checkbox" name=aihao value="3" >
            <br>
            城市:
            <select name="address">
                <option >--请选择--</option>
                <option value="1">北京</option>
                <option value="2">上海</option>
                <option value="3" selected="selected">重庆</option>
            </select>
            <br>
            文本域:<br>
            <textarea name="text" rows="10" cols="20"></textarea>
            <br>
            <input type="submit" value="登陆">

        </form>
    </body>
</html>
```

