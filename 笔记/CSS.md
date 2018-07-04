### 三、CSS标准

> 引入案例：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			h2{
> 				color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<!--<h2>
> 			<font color="red">标题一</font>
> 		</h2>
> 		<p>段落一</p>
> 		
> 		<h2>
> 			<font color="red">标题二</font>
> 		</h2>
> 		<p>段落二</p>
> 		
> 		<h2>
> 			<font color="blue">标题二</font>
> 		</h2>
> 		<p>段落三</p>
> 		
> 		<h2>
> 			<font color="blue">标题一</font>
> 		</h2>
> 		<p>段落一</p>
> 		
> 		<h2>
> 			<font color="blue">标题一</font>
> 		</h2>
> 		<p>段落一</p>-->
> 		
> 		<h2>bhbjh</h2>
> 		<h2>bdgn</h2>
> 		<h2>nhtn</h2>
> 		
> 	</body>
> </html>
> ```
>
> 为了解决html结构和表现混杂在一起的问题，引入css
>
> css:Cascading Style Sheet,层叠样式表，主要用于控制网页样式并且允许将样式信息和网页内容分离
>
> 辅助html设置标签的样式
>
> 层叠：使用不同的方式为同一个标签设置不同的样式，最后将所有的样式层叠到一起，共同作用于这个标签
>
> 传统的html的缺点：
>
> ​	a.维护困难【为了修改某个标签的某个属性花费大量的时间】
>
> ​	b.标签是有限的【文字间距，段落缩进等】
>
> ​	c.网页过“胖”【没有统一的方式对标签设置样式】
>
> ​	d.定位困难【直接定位到需要使用的标签对象】
>
> ```
> 注释：/*
> 	*xxxxxxxxx
> 	*xxxxxxxx
> 	*/
> 快捷键：ctrl + /
> ```

### 四、CSS的核心基础

#### 1.语法规则

> 举例：描述一个人的特征，列出一张表
>
> 张飞{
>
> ​	身高：144cm;
>
> ​	体重：80kg；
>
> ​	性别：男；
>
> }
>
> 三要素组成:姓名，属性和属性值
>
> 标题{
>
> ​	字体：宋体；
>
> ​	字号：15像素；
>
> ​	颜色：红色；
>
> ​	装饰：下划线；
>
> }
>
> h2{
>
> ​	font-family:宋体；
>
> ​	font-size:15px;
>
> ​	color:red;
>
> ​	text-decoration:underline;
>
> }
>
> CSS操作的思想：首先明确对数什么对象进行设置，明确对该对象的哪个方面需要设置，明确需要设置的值【对象，属性，值】
>
> CSS的核心：选择器
>
> 选择器：为了能够使得CSS规则和html标签对应起来，就必须定义一套完整的规则，实现CSS对html标签的选择
>
> 语法：
>
> 选择器{
>
> ​	属性1：属性值1；
>
> ​	属性2：属性值2；
>
> ​	。。。。
>
> }
>
> 分类：通配符选择器，标签名称选择器，类选择器，id选择器，属性选择器，包含选择器，伪类选择器，结构选择器，组合选择器

#### 2.选择器

> <style></style>:选择器全部书写在标签之间

##### 2.1通配符选择器

> 语法：
>
> *{
>
> }
>
> 作用：可以给当前页面中所有的标前对象设置指定的样式
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			/*通配符选择器*/
> 			*{
> 				color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<h1>hello</h1>
> 		<p>html</p>
> 	</body>
> </html>
> ```

##### 2.2标签名称选择器

> 语法：
>
> 标签名称{
>
> }
>
> 作用：只设置指定标签的样式
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			/*标签名称选择器*/
> 			h1{
> 				color: red;
> 			}
> 			p{
> 				color: blue;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<h1>hello</h1>
> 		<h1>64276572</h1>
> 		<p>html</p>
> 	</body>
> </html>
> ```
>
> 

##### 2.3类选择器

> class
>
> 语法：
>
> .类名{
>
> }	
>
> 说明：类选择器主要是结合class属性使用，类名需要自定义
>
> 作用：是在标签名称选择器的基础上，设置一些特殊的情况
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			h1{
> 				color: red;
> 			}
> 			p{
> 				color: blue;
> 			}
> 			
> 			/*类选择器*/
> 			.green{
> 				color: green;
> 			}
> 			.yellow{
> 				color: yellow;
> 			}
> 			
> 			.big{
> 				font-size: 30px;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<h1>升职加薪，迎娶白富美</h1>
> 		<h1 class="green">hello</h1>
> 		<p>还是踏踏实实工作把</p>
> 		<p class="yellow">html</p>
> 		
> 		<!--同一个类选择器可以作用于不同的标签-->
> 		<font class="green">1241241</font>
> 		
> 		<!--不同的类选择器可以同时作用于同一个标签-->
> 		<!--好处：可以适当减少代码量-->
> 		<font class="yellow big">today is a good day</font>
> 		
> 	</body>
> </html>
> ```

##### 2.4id选择器

> ```
> 语法：
> #id值{
>   
> }
> ```
>
> 作用：使用和类选择器的使用是类似的，为了给特殊的标签设置样式
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			#bold{
> 				font-weight: bold;
> 			}
> 			#color{
> 				color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<p id="bold">轻轻的我走了</p>
> 		<p id="color">正如我轻轻地来</p>
> 		
> 		<!--注意1：将同一个ID选择器作用于不同的标签，可以使用-->
> 		<!--但是：不建议这么做，js中的函数getElementById()的作用是通过id获取对应的标签对象，
> 			为了保证每次获取到的标签对象是唯一的，id选择器只使用一次
> 			
> 		-->
> 		<!--<p id="bold">我挥一挥衣袖</p>-->
> 		
> 		<!--注意2:多个id选择器不能同时作用于同一个标签-->
> 		<!--<p id="bold color">不带走一片云彩</p>-->
> 	</body>
> </html>
> ```

##### 2.5属性选择器

> 语法：
>
> 选择器[属性名]{
>
> }
>
> 选择器[属性名=属性值]{
>
> }
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			/*注意：属性选择器中的选择器可以是任意的选择器【标签名称，类，id】*/
> 			/*p[name]{
> 				color: purple;
> 			}
> 			p[name="aaa"]{
> 				color: purple;
> 			}*/
> 			
> 			#abc[name="ccc"]{
> 				color: cyan;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<p name="aaa">hello</p>
> 		<p name="bbb">hello~~~</p>
> 		<p id="abc" name="ccc">abcd</p>
> 		<p id="abc" name="ddd">abcdef</p>
> 	</body>
> </html>
> ```

### 一、上堂回顾

> 1.html
>
> ​	a:
>
> ​		属性:href,target[_self,_blank]
>
> ​		定位资源#:  #top    #id
>
> ​	音视频标签：audio   video
>
> ​		autoplay controls loop
> ​	表单标签
>
> ​		标签：form  input   select  textarea
>
> ​		属性：type：text，password，radio，checkbox，file，button，submit，reset
>
> ​			    name：
>
> ​			    value
>
> ​			    id
>
> ​			   class
>
> ​			   checked
>
> ​			   selected
>
> ​		get和post之间的区别
>
> ​	头标签：head
>
> ​			link
>
> 2.css
>
> ​	什么是css，作用是什么
>
> ​	层叠样式表，控制网页的样式并且将设置的样式作用于指定的html标签
>
> ​	意义：为了将html和css样式分离，为了代码的可读性，后期的可维护性
>
> ​	<style></style>:head的子标签

### 二、CSS选择器

#### 1.基本选择器

> ```
> 1.通配符选择器
> *{}
> 
> 2.标签名称选择器
> 标签名称{}
> 
> 3.类选择器
> .class的值{}
> 
> 4.ID选择器
> #id的值{}
> 
> 5.属性选择器【过滤选择器】
> 基本选择器[属性]{}
> 基本选择器[属性=值]{}
> ```

#### 6.包含选择器

> 父子标签   或者  先辈后辈标签
> a.查找父子标签或者先辈后辈标签
> 先辈标签选择器 后辈标签选择器{}
> 父标签选择器	子标签选择器{}
> b.查找直接的子标签  后辈标签
> 父标签选择器  >  子标签选择器{}
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<style>
> 		/*包含选择器*/
> 		
> 		/*父子标签，先辈后辈标签，但是，一般采用这种选择器查找的是先辈后辈标签*/
> 		/*div p{
> 			color:red
> 		}*/
> 		
> 		/*父子标签*/
> 		/*div > p{
> 			color: blue;
> 		}*/
> 		
> 		#box > p{
> 			color: blue;
> 		}
> 		
> 		/*注意：包含选择器完全由基本选择器组成，没有任何限制*/
> 		
> 		</style>
> 	</head>
> 	<body>
> 		<div id="box">
> 			<p>第一个p标签</p>
> 			<span>
> 				<p>第二个p标签</p>
> 			</span>
> 		</div>
> 	</body>
> </html>
> ```

#### 7.伪类选择器

> 注意：其中的选择器也是可以是任意的基本选择器
> 选择器:hover{}  :设置鼠标的悬浮事件
> 选择器:before{}  :添加头部
> 选择器:after{}  :添加尾部
> 选择器:first-letter{}  :设置第一个字符的样式
> 选择器:first-line{}  :设置第一行的样式
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 		/*伪类选择器*/
> 		/*hover：鼠标悬浮事件*/
> 		/*#first:hover{
> 			color:red;
> 			font-size: 30px;
> 		}
> 		
> 		p:hover{
> 			color:red;
> 			font-size: 30px;
> 		}*/
> 		
> 		/*添加头部*/
> 		#first:before{
> 			content: "这是头部";
> 		}
> 		
> 		/*添加尾部*/
> 		#first:after{
> 			content: "last";
> 		}
> 		
> 		/*设置第一个字符的样式*/
> 		#first:first-letter{
> 			font-size: 30px;
> 		}
> 		
> 		/*设置第一行的样式*/
> 		#first:first-line{
> 			text-decoration: underline;
> 		}
> 		
> 		</style>
> 	</head>
> 	<body>
> 		<p id="first">世上无难事</p>
> 		<p>只怕有心人</p>
> 	</body>
> </html>
> ```

#### 8.结构选择器

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			/*结构选择器*/
> 			/*需求：将ul下面的第一个li设置样式*/
> 			ul li:first-child{
> 				color:red;
> 			}
> 			
> 			ul li:last-child{
> 				color:red;
> 			}
> 			
> 			/*顺序查找*/
> 			/*
> 			 * number:第几个子标签
> 			 * odd:奇数行
> 			 * even：偶数行
> 			 */
> 			/*注意：子标签的编号是从1开始的*/
> 			ul li:nth-child(odd){
> 				color: blue;
> 			}
> 			
> 			/*倒序查找*/
> 			ul li:nth-last-child(2){
> 				color: cyan;
> 			}
> 			
> 			/*查找空标签【文本为空】*/
> 			li:empty{
> 				background-color: purple;
> 			}
> 			
> 			/*设置否定标签的样式*/
> 			li:not(#aaa){
> 				font-size: 20px;
> 				color: pink;
> 			}
> 			
> 		/*注意：结构选择器：选择器可以是任意的基本选择器，本质上过滤选择器*/
> 		</style>
> 	</head>
> 	<body>
> 		<ul>
> 			<li>1111</li>
> 			<li>2222</li>
> 			<li>3333</li>
> 			<li id="aaa">4444</li>
> 			<li>5555</li>
> 			<li></li>
> 			<li>6666</li>
> 		</ul>
> 	</body>
> </html>
> ```

#### 9.组合选择器

> 语法：
>
> 选择器1，选择器2，。。。{
>
> }
>
> 作用：简化代码
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 		/*组合选择器*/
> 		/*h1,p,span{
> 			color:red;
> 		}*/
> 		
> 		#header,p,span{
> 			color:red;
> 		}
> 		
> 		</style>
> 	</head>
> 	<body>
> 		<h1 id="header">标题</h1>
> 		<p>段落</p>
> 		<span>hello</span>
> 		<h1>标题</h1>
> 		<p>段落</p>
> 		<span>hello</span>
> 	</body>
> </html>
> ```

#### 10.选择器练习

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			/*通配符选择器*/
> 			*{
> 				background-color: lightgray;
> 			}
> 			/*标签名称选择器*/
> 			p{
> 				text-indent: 2em;
> 			}
> 			/*id选择器*/
> 			#first{
> 				background-color: yellow;
> 			}
> 			/*类选择器*/
> 			.little{
> 				font-weight: 200;
> 			}
> 			.pink{
> 				color: pink;
> 			}
> 			/*属性选择器*/
> 			p[name]{
> 				font-family: "楷体";
> 			}
> 			p[name="good"]{
> 				text-decoration: underline;
> 			}
> 			
> 	
> 			/*包含选择器*/
> 			/*#box span{
> 				border:2px dashed orange
> 			}*/
> 			
> 			#box > span{
> 				border:2px dashed blue
> 			}
> 			
> 			/*伪类选择器*/
> 			#first:hover{
> 				font-size: 50px;
> 			}
> 			
> 			/*结构选择器*/
> 			body p:nth-child(6){
> 				color: cyan;
> 			}
> 			
> 			/*组合选择器*/
> 			#first,.pink{
> 				background-color: darkcyan;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<p id="first">盼望着，盼望着，东风来了，春天的脚步近了。 </p>
> 		<p class="little pink">一切都像刚睡醒的样子，欣欣然张开了眼。山朗润起来了，水涨起来了，太阳的脸红起来了。 </p>
> 		<p class="pink">小草偷偷地从土地里钻出来，嫩嫩的，绿绿的。园子里，田野里，瞧去，一大片一大片满是的。坐着，躺着，打两个滚，踢几脚球，赛几趟跑，捉几回迷藏。风轻俏俏的，草软绵绵的。 </p>
> 		<p name="tree">桃树，杏树，梨树，你不让我，我不让你，都开满了花赶趟儿。<br/>红的像火，粉的像霞，白的像雪。花里带着甜味；闭了眼，树上仿佛已经满是桃儿，杏儿，梨儿。花下成千成百的蜜蜂嗡嗡的闹着，大小的蝴蝶飞来飞去。野花遍地是：杂样儿，有名字的，没名字的，散在草丛里像眼睛像星星，还眨呀眨。 </p>
> 		<p name="good">“吹面不寒杨柳风”，不错的，像母亲的手抚摸着你，风里带着些心翻的泥土的气息，混着青草味儿，还有各种花的香，都在微微润湿的空气里酝酿。鸟儿将巢安在繁花嫩叶当中，高兴起来，呼朋引伴的卖弄清脆的歌喉，唱出婉转的曲子，跟清风流水应和着。牛背上牧童的短笛，这时候也成天嘹亮的响着。 </p>
> 		<p>雨是最寻常的，一下就是三两天。可别恼。看，像牛牦，像花针，像细丝，密密的斜织着，人家屋顶上全笼着一层薄烟。树叶却绿得发亮，小草也青得逼你的眼。傍晚时候，上灯了，一点点黄晕的光，烘托出一片安静而和平的夜。在乡下，小路上，石桥边，有撑着伞慢慢走着的人，地里还有工作的农民，披着所戴着笠。他们的房屋稀稀疏疏的，在雨里静默着。</p>
>  		<p>天上的风筝渐渐多了，地上的孩子也多了。城里乡下，家家户户，老老小小，也赶趟似的，一个个都出来了。舒活舒活筋骨，抖擞抖擞精神，各做各的一份事儿去。“一年之计在于春”，刚起头儿，有的是功夫，有的是希望 </p>
>  		
>  		<div id="box">
>  			<span>春天像刚落地的娃娃，从头到脚都是新的，它生长着。 </span>
> 			<p><span>春天像小姑娘，花枝招展的笑着走着。</span> </p>
> 			<p>春天像健壮的青年，有铁一般的胳膊和腰脚，领着我们向前去。</p>
>  		</div>
> 	</body>
> </html>
> ```

### 三、CSS和html的结合方式

#### 1.行内样式

> 每个html标签都有一个属性：style
>
> 缺点:当需要设置的属性比较多的时候，网页过胖，css和html不分离
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<!--行内样式-->
> 		<p style="color: red;background-color: blue;font-weight: 200;"></p>
> 	</body>
> </html>
> ```

#### 2.内嵌样式

> 将css代码写在head中，需要在style标签中进行声明
>
> 好处：将所有的css代码集中到了同一个区域中，方便后期维护
>
> 缺点：维护成本高
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style type="text/css">
> 			p{
> 				color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<p></p>
> 	</body>
> </html>
> ```

#### 3.链接样式

> 使用频率最高，用法：新建一个单独的css文件，将对应的选择器全部书写在该文件中
>
> 使用：在需要用到的html文件中需要通过<link>链接
>
> <link href="css/style1.css" type="text/css" rel="stylesheet"/>
>
> href:需要链接的资源的路径【相对路径】
>
> type：标记文档的类型，格式：大类型/小类型
>
> ​	text/css:css类型
>
> ​	text/javascript:javascript类型
>
> ​	image/jpg:  jpg图片
>
> rel:relationship
>
> ​	stylesheet:样式表
>
> ​	 rel="stylesheet"：描述的是当前页面和href所指定的css文件之间的关系
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--链接样式-->
> 		<link href="css/style1.css" type="text/css" rel="stylesheet"/>
> 	</head>
> 	<body>
> 		<h1>title</h1>
> 		<span id="span">hello</span>
> 	</body>
> </html>
> ```

#### 4.导入样式

> 通过@import将外部的css文件导入到当前的html文件中
>
> 注意：需要将@import url(相对路径)写在style标签中
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style type="text/css">
> 			@import url("css/style1.css")
> 		</style>
> 	</head>
> 	<body>
> 		<h1>title</h1>
> 		<span id="span">hello</span>
> 	</body>
> </html>
> ```

#### 5.各种样式之间的优先级问题

> 结论一：行内，内嵌，导入：行内样式的优先级最高
>
> 结论二：链接样式和导入样式统称为外部样式，出现在后面的则作用于指定的标签
>
> 结论三：导入 样式和内嵌样式同时出现在style标签的时候，如果导入样式在内嵌样式的前面，则任何一种样式都不起作用；反之，则起作用的是内嵌样式
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		
> 		<link href="css/green.css" type="text/css" rel="stylesheet" />
> 		<style>
> 			
> 			/*p{
> 				color:blue;
> 			}*/
> 			@import url("css/red.css" )
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<!--<p style="color: purple;">hello</p>-->
> 		<p>hello</p>
> 	</body>
> </html>
> ```
>
> 总结：
>
> ​	作用范围：
>
> ​	行内样式:仅作用于当前的标签
>
> ​	内嵌样式：仅作用于当前的html页面
>
> ​	外部样式：关联该css文件的html页面
>
> 注意：在实际项目中，结合方式1~2种
>
> ​	使用最多：学习是内嵌样式，工作是链接样式

### 四、CSS的属性

#### 1.字体属性

> font:size   color
>
> font-family:字体类型，比如：宋体，楷体
>
> font-style：设置是否倾斜
>
> ​	normal：正常
>
> ​	italic:意大利体
>
> ​	oblique：斜体
>
> font-weight:设置字体的粗细，取值范围为100~900，数值越大，则表示字体越粗
>
> ​	normal：正常
>
> ​	bold：粗体
>
> ​	bolder：
>
> ​	lighter：
>
> font-size:字体大小，用px作为单位，默认字体大小为16px
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			p{
> 				/*
> 				 * 为了适配【兼容】
> 				 */
> 				font-family: 黑体,宋体,Arial;
> 				
> 				font-style: italic;
> 				
> 				font-weight: bold;
> 				
> 				font-size: 10px;
> 				/*
> 				 * px:像素，与分辨率有关，如果缩放则不推荐使用
> 				 * em：使用尺寸，主要方便字体的放大和缩小
> 				 * 1em = 16px
> 				 */
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<p>字体属性</p>
> 	</body>
> </html>
> ```

#### 2.文本属性

> text-decoration:设置文字的装饰效果
>
> ​	none：
>
> ​	underline：下划线
>
> ​	line-through:给文字添加删除线
>
> ​	overline：为文字添加顶线
>
> ​	blink：文字闪烁，仅部分浏览器支持
>
> text-indent:段落缩进，中文中常用2em
>
> text-align:对齐方式
>
> ​	left
>
> ​	right
>
> ​	center：居中
>
> ​	justify:两端对齐
>
> letter-spacing：英文，设置单词内部的字母之间的间距
>
> word-spacing:单词之间的间距
>
> text-transform:大小写转换，英文
>
> ​	none：
>
> ​	capitalize：单词首字母大写 
>
> ​	uppercase：小写换大写
>
> ​	lowercase:大写转小写
>
> direction：文本方向
>
> ​	ltr:从左到右，默认
>
> ​	rtl:向右到左
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			p{
> 				text-decoration: line-through;
> 				
> 				text-indent: 2em;
> 				
> 				/*alignment*/
> 				/*text-align: center;*/
> 				
> 				/*单词中的字母之间/中文文字之间的间距*/
> 				letter-spacing: 10px;
> 				/*英文单词之间的间距*/
> 				word-spacing: 30px;
> 				
> 				/*capitalize:原来的大写字母保留，将每个单词的首字母大写*/
> 				text-transform: capitalize;
> 				
> 				direction: rtl;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<p>tOdaY is gooD day好日子</p>
> 	</body>
> </html>
> ```

#### 3.盒子属性

> div
>
> 1>边框属性
>
> ​	border：设置变量，统一设置，参数：边框宽度  边框样式 边框颜色
>
> ​		border-top；
>
> ​		border-right:
>
> ​		border-bottom:
>
> ​		border-left；
>
> ​	border-width:设置边框的宽度
>
> ​	border-style:边框样式
>
> ​		dotted:点画线
>
> ​		dashed:虚线
>
> ​		solid：实线
>
> ​		double：双线
>
> ​	border-color:边框颜色
>
> ​	border-redius:边框削圆角【一般采用百分比，百分比越大，表示圆角越大，当一个矩形为正方向的时候，取值为50%，则形成一个圆，大于50%的时候，仍然为一个圆】
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			div{
> 				width:200px;
> 				height: 200px;
> 				/*border: 2px dashed blue;*/
> 			}
> 			
> 			#div2{
> 				border-right: 2px dotted red;
> 				border-bottom: 2px dotted red;
> 				border-left: 2px dotted red;
> 				border-top: 2px dotted red;
> 				
> 				border-radius: 30%;
> 			}
> 			
> 			#div3{
> 				border-width: 4px;
> 				border-style: solid;
> 				border-color: orange green red blue;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div>AAAAAAAA</div>
> 		<div id="div2">ABBBBBB</div>
> 		<div id="div3">CCCCCCC</div>
> 		
> 	</body>
> </html>
> ```
>
> 注意事项：
>
> ​	border-style、border-color，border-width根据参数的不同结果不同
>
> ​	1个：设置的是上下左右全部
>
> ​	2个：前者设置的是上下，后者设置的左右
>
> ​	3个：前者表示上，中间表示左右，后者表示下
>
> ​	4个：分别表示上右下左
>
> 2>内边距
>
> ​	padding：参数为距离，统一设置
>
> ​		padding-top：
>
> ​		padding-right：
>
> ​		padding-bottom		
>
> ​		padding-left		
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			div{
> 				width:200px;
> 				height: 200px;
> 				border: 2px dashed blue;
> 			}
> 			
> 			#div2{
> 				padding: 20px;
> 			}
> 			
> 			#div3{
> 				padding-right: 30px;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<div>AAAAAAAA</div>
> 		<div id="div2">ABBBBBB</div>
> 		<div id="div3">CCCCCCC</div>
> 	</body>
> </html>
> ```
>
> 3>外边距
>
> ​	margin：参数为距离，统一设置
>
> ​		margin-top：
>
> ​		margin-right：
>
> ​		margin-bottom		
>
> ​		margin-left	
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			div{
> 				width:200px;
> 				height: 200px;
> 				border: 2px dashed blue;
> 			}
> 			
> 			#div2{
> 				margin: 20px;
> 			}
> 			
> 			#div3{
> 				margin-left: 30px;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<div>AAAAAAAA</div>
> 		<div id="div2">ABBBBBB</div>
> 		<div id="div3">CCCCCCC</div>
> 	</body>
> </html>
> ```
>
> 盒子属性：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			img{
> 				width: 400px;
> 				height: 400px;
> 				border-left-color:red ;
> 				border-left-style: dashed;
> 				border-left-width: 2px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<img src="img/pic20.jpg" />
> 	</body>
> </html>
> ```

#### 4.尺寸属性

> width：宽度
>
> height：高度
>
> line-height:行高
>
> 注意事项：当文本内容只有一行的时候，将line-height=height,则文本内容在垂直方向上居中显示；水平方向上的居中的显示：text-align:center;
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			div{
> 				width: 100%;
> 				height:400px;
> 				background-color: red;
> 				text-align: center;
> 				line-height: 50px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div>
> 			尺寸属性 this is a text
> 			尺寸属性 this is a text
> 			尺寸属性 this is a text尺寸属性 this is a text
> 			尺寸属性 this is a text
> 			尺寸属性 this is a text
> 			尺寸属性 this is a text
> 			
> 		</div>
> 	</body>
> </html>
> ```

#### 5.背景属性

> background:背景色/图
>
> background-color：背景色
>
> background-image：背景图    url(图片的路径)
>
> background-repeat：是否需要设置背景的平铺效果
>
> ​	repeat:默认值，水平和垂直方向平铺
>
> ​	no-repeat:不平铺
>
> ​	repeat-x:水平
>
> ​	repeat-y：垂直
>
> background-position：背景位置
>
> ​	top，left，right，bottom，center
>
> background-attachment设置背景图随着网页内容一起滚动
>
> ​	scroll：滚动
>
> ​	fixed：固定
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			body{
> 				width: 100%;
> 				height: 9999px;
> 				
> 				
> 				/*背景色*/
> 				/*background-color: red;*/
> 				
> 				/*background-image: url(img/pic20.jpg);*/
> 				
> 				background-repeat: no-repeat;
> 				
> 				background-attachment: fixed;
> 				
> 				/*设置背景色的渐变效果*/
> 				/*线性渐变,默认为从上往下*/
> 				/*background: linear-gradient(red,blue);*/
> 				
> 				/*从左到右*/
> 				/*background: linear-gradient(to right,red,blue);*/
> 				
> 				/*从左上角到右下角*/
> 				background: linear-gradient(to bottom right,red,blue);
> 			}
> 		</style>
> 	</head>
> 	<body>
> 	</body>
> </html>
> ```

#### 6.和列表有关的属性【了解】

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			li{
> 				background-color: orange;
> 				/*修改项目符号的样式*/
> 				/*list-style-type: none;*/
> 				
> 				/*将项目符号设置为自定义的图片*/
> 				/*list-style-image: url(img/pic20.jpg);*/
> 				
> 				/*设置项目符号的位置*/
> 				/*list-style-position: inside;*/
> 				
> 				/*合并，参数：自定义图片的路径  位置*/
> 				list-style:url(img/pic20.jpg) inside;
> 				
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<ul>
> 			<li>苹果</li>
> 			<li>香蕉</li>
> 			<li>荔枝</li>
> 			<li>西瓜</li>
> 		</ul>
> 	</body>
> </html>
> ```

#### 7.浮动属性【重要】

> div是块级元素，在页面中独占一行，可以换行，默认从上往下依次排列，这种排列的方式被称为流
>
> 元素浮动之前，存在于标准流中，是竖向排列的
>
> 元素浮动之后，可以变为横向排列
>
> 本质：将默认竖向排列的元素变为横向排列
>
> float：
>
> ​	none：
>
> ​	left：将该标签浮动在左侧
>
> ​	right：将该标签浮动在右侧
>
> clear：清除浮动，取值一般为left或者right，表示将 原来设置的浮动清除掉，为了不影响后面标签的位置
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			#div1{
> 				width: 100px;
> 				height: 100px;
> 				border: 1px dashed red;
> 				float: right;	
> 			}
> 			
> 			#div2{
> 				width: 200px;
> 				height: 200px;
> 				border: 1px dashed blue;	
> 				float: right;
> 			}
> 			
> 			#div3{
> 				width: 400px;
> 				height: 400px;
> 				border: 1px dashed green;	
> 				float: right;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<div id="div1">AAAAA</div>
> 		<div id="div2">BBBBB</div>
> 		<div id="div3">CCCCC</div>
> 	</body>
> </html>
> ```
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			li{
> 				float: left;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<ul>
> 			<li>4245</li>
> 			<li>436</li>
> 			<li>6436</li>
> 			<li>6346</li>
> 			<li>643</li>
> 		</ul>
> 	</body>
> </html>
> ```

### 一、上堂回顾

> 1.选择器
>
> ​	包含：
>
> ​		选择器1 选择器2{}：父子标签和先辈后辈标签
>
> ​		选择器1 > 选择器2{}:父子标签
>
> ​	伪类选择器：hover
>
> ​	结构：first-child       nth-child(num)    子标签
>
> ​	组合：逗号
>
> 2.css和html的结合方式
>
> ​	内部样式：在当前html页面中直接使用css
>
> ​	行内
>
> ​	内嵌：style书写选择器
>
> ​	外部样式：在当前html页面引入的外部的css文件
>
> ​	链接：link：href
>
> ​	导入：@import url()
>
> 3.属性

### 二、CSS属性

#### 浮动属性之图文混排

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<style>
> 			/*背景*/
> 			body{
> 				background-color: lightgray;
> 				margin: 0px;
> 				padding: 0px;
> 			}
> 			img{
> 				width: 150px;
> 				height: 200px;
> 				float: left;
> 			}
> 			p{
> 				text-indent: 2em;
> 				padding: 10px;
> 			}
> 			
> 			span{
> 				font-size: 50px;
> 				font-family: 黑体;
> 				font-weight: bold;
> 				float: left;
> 			}
> 			
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<img src="img/zuchongzhi.png" />
> 		<p><span>祖</span>冲之，429年（南朝宋元嘉六年）出生于建康（今南京），祖籍范阳郡遒县（今河北涞水县）。西晋末期，北方发生大规模战乱，祖冲之的先辈从河北迁徙到江南，并在江南定居下来。祖冲之就出生在江南，其祖父祖昌任刘宋朝大匠卿，是朝廷管理土木工程的官吏，父亲祖朔之做“奉朝请”，学识渊博，常被邀请参加皇室的典礼、宴会。</p>
> 
> 
> 		<p>祖冲之从小就受到很好的家庭教育。爷爷给他讲“斗转星移”，父亲领他读经书典籍，家庭的熏陶，耳濡目染，加之自己的勤奋，使他对自然科学和文学、哲学，特别是天文学产生了浓厚的兴趣，在青年时代就有了博学的名声</p>
> 
> 		<p>祖冲之从小就受到很好的家庭教育。爷爷给他讲“斗转星移”，父亲领他读经书典籍，家庭的熏陶，耳濡目染，加之自己的勤奋，使他对自然科学和文学、哲学，特别是天文学产生了浓厚的兴趣，在青年时代就有了博学的名声</p>
> 
> 		<p>由于祖冲之博学多才的名声，被南朝宋孝武帝派至当时朝廷的学术研究机关华林学省做研究工作，后来又到总明观任职。当时的总明观是全国最高的科研学术机构，相当于现在的中国科学院。总明观内分设文、史、儒、道、阴阳5门学科，实行分科教授制度，请来各地有名望的学者任教，祖冲之就是其一。在这里，祖冲之接触了大量国家藏书，包括天文、历法、术算方面的书籍，具备了借鉴与拓展的先决条件。</p>
> 	</body>
> </html>
> ```

#### 1.显示属性

> display：标签的显示状态
>
> ​	block：块级标签
>
> ​		      特点:总是以一个块的形式表现出来，可以独占一行
>
> ​			       可以设置宽高以及内外边距，如果不设置宽，默认和父标签的宽相等
>
> ​		      例如：div   li   p   hn
>
> ​	inline：行内标签
>
> ​			特点：不会自动换行，宽高随着内容自适应，设置宽高以及内外边距无效
>
> ​			例如：span  a
>
> ​			注意：设置这个值，可以将一个块级标签转换为行内标签，那么这个块级标签将不能再设置宽高以及内外边距
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			*{
> 				padding: 0px;
> 				margin: 0px;
> 				list-style: none;
> 			}
> 			
> 			ul li{
> 				float: left;
> 			}
> 			
> 			a{
> 				/*将a行内标签转换为块级标签*/
> 				display: block;
> 				width: 30px;
> 				height: 30px;
> 				margin: 5px;
> 				text-decoration: none;
> 				text-align: center;
> 				line-height: 30px;
> 				border: 1px solid red;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<ul>
> 			<li><a href="">1</a></li>
> 			<li><a href="">2</a></li>
> 			<li><a href="">3</a></li>
> 			<li><a href="">4</a></li>
> 			<li><a href="">5</a></li>
> 			<li><a href="">6</a></li>
> 		</ul>
> 	</body>
> </html>
> ```
>
> ​	inline-block：行内块级标签
>
> ​			特点：不但具有block标签可以设置宽高以及内外边距的特性，还具有inline标签不换行的特性
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			ul,li,a,*{
> 				padding: 0px;
> 				margin: 0px;
> 				list-style: none;
> 				text-decoration: none;
> 			}
> 			
> 			li{
> 				/*设置display属性的值inline-block，li将不再自动换行，呈现横向排列*/
> 				display: inline-block;
> 				border: 1px solid red;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<ul>
> 			<li><a href="">1</a></li><li><a href="">2</a></li><li><a href="">3</a></li><li><a href="">4</a></li>
> 			<li><a href="">5</a></li>
> 			<li><a href="">6</a></li>
> 		</ul>
> 		
> 		<!--
> 			所有的内外边距设置为了0，但是呈现的效果还是有间距
> 			原因：inline的特点：在浏览器中，空白符是不会被忽略的，换行会产生空白符
> 			解决：li标签之间的换行消除掉
> 		-->
> 		
> 	</body>
> </html>
> ```
>
> ​	none:隐藏状态
>
> ​			特点：既不会占用浏览器中的空间，也无法显示，相当于该元素不存在
>
> ​			作用：动画，改善页面的重排效果	

#### 2.定位属性

> position：标签的位置

##### 2.1绝对定位

> absolute：绝对定位，使用top，bottom等设置位置
>
> ​		参照物：该标签的父标签或者先辈标签是否被设置了有效的定位属性
>
> ​		帮助理解：如果一个标签设置了绝对定位之后，该标签随着父标签或者先辈标签的位置的变化而变化
>
> ​		特点：会脱离文档流，不会保留位置
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title>相对定位</title>
> 		<style>
> 			.left{
> 				position: relative;
> 				left:-20px;
> 			}
> 			.right{
> 				position: relative;
> 				left: 20px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<h2>标题标题标题标题标题</h2>
> 		<h2 class="left">标题标题标题标题标题</h2>
> 		<h2 class="right">标题标题标题标题标题</h2>
> 		<!--相对定位：会按照元素的原始位置对该元素进行移动，移动的距离取决于left，top，right以及bottom的取值-->
> 	</body>
> </html>
> ```

##### 2.2相对定位

> relative：相对定位，使用top，bottom等设置位置
>
> ​		参照物：该标签自身原来的位置
>
> ​		特点:不会脱离文档流，会保留自己的位置【灵魂脱壳】
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title>绝对定位</title>
> 		<style>
> 			body{
> 				background-color: lightcyan;
> 				height: 5000px;
> 			}
> 			.h{
> 				position: absolute;
> 				left: 100px;
> 				top: 300px;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>	
> 		
> 		<h2 class="h">标题标题标题标题标题标题标题</h2>
> 		
> 	</body>
> </html>
> ```

##### 2.3固定定位

> fixed：固定定位	
>
> ​	特点：固定在一个位置不发生改变，主要用于广告中
>
> ​	有效的定位属性可以设置举例参照物的left，top，right，bottom的值，如果在参照物的内部，这些属性的值为正数表示在浏览器的可见范围内，如果未负数则表示超出浏览器的边界
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			body{
> 				height: 5000px;
> 			}
> 			
> 			#one{
> 				position: fixed;
> 				left: 10px;
> 				top: 10px;
> 			}
> 			
> 			#second{
> 				position: fixed;
> 				right: 30px;
> 				bottom: 100px;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<p id="one">文本</p>
> 		<p id="second">hello</p>
> 	</body>
> </html>
> ```

##### 2.4z-index的使用

> z-index
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			img{
> 				position: absolute;
> 				left: 0px;
> 				top: 0px;
> 				
> 				/*
> 				 * 当出现标签重叠的情况下
> 				 * 根据z-index的值决定哪个标签需要在最上层
> 				 * z-index的默认值为0，取值越大，则被层叠在最上层
> 				 * 在使用z-index必须使用position属性
> 				 */
> 				z-index:1;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<h1>这是一个标题</h1>
> 		<img src="img/zuchongzhi.png" width="200px" height="200px" />
> 	</body>
> </html>
> ```

#### 3.形变和过渡

> 形变：transform
>
> 过渡：transition

##### 3.1形变

> rotate(deg):指定的标签需要旋转的度数
>
> scale(num):指定的标签拉伸和缩放
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			#transform{
> 				width: 200px;
> 				height: 200px;
> 				background-color: orange;
> 				
> 				margin: 50px;
> 				
> 				/*设置旋转点*/
> 				/*center left right top bottom*/
> 				transform-origin:center left;
> 				
> 				/*设置旋转的角度*/
> 				/*默认沿着z轴旋转的： rotate()*/
> 				/* rotateX()    rotateY()*/
> 				/*degree*/
> 				/*transform:rotate(30deg);*/ 
> 				
> 				/*拉伸形变*/
> 				/*默认情况下横向拉伸和纵向拉伸是同时进行的*/
> 				/*scaleX()   scaleY()*/
> 				/*transform: scale(2);*/
> 				
> 				transform:rotate(30deg) scale(2);
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="transform"></div>
> 	</body>
> </html>
> ```

##### 3.2过渡

> transition-duration：过渡的时间
>
> transition-property：需要过渡的标签【all】
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			div{
> 				width: 200px;
> 				height: 200px;
> 				background-color: red;
> 				
> 				transform: rotate(-90deg);
> 				
> 				margin: 100px;
> 				
> 				color: white;
> 				
> 				
> 				/*添加过渡需要注意两点
> 				 * 哪个属性需要过渡
> 				 * 发生过渡需要的时间
> 				 */
> 				transition-duration:5s;
> 				transition-property: all;
> 			}
> 			
> 			div:hover{
> 				background-color: yellow;
> 				transform: rotate(90deg);
> 				font-size: 30px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div>过渡</div>
> 	</body>
> </html>
> ```

#### 4.动画

> animation：动画的名称【自定义】 动画持续的时间   动画的类型【线性和非线性】
>
> @keyframes  动画的名称{
>
> ​	from{}
>
> ​	to{}
>
> }
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			div{
> 				background-color: red;
> 				width: 200px;
> 				height: 200px;
> 				
> 				/*
> 				 * 可以设置动画持续的时间，默认为1次，如果无限次：infinite
> 				 * 动画的类型：linear 线性动画
> 				 * 	          ease：由快到慢
> 				 */
> 				animation: animate 5s linear;
> 			}
> 			
> 			/*制作动画*/
> 			/*
> 			 * from ~  to   ======>0% ~ 100%
> 			 * 动画的开始状态  ~ 动画的结束状态
> 			 */
> 			@keyframes animate{
> 				/*from{
> 					margin-left: 50px;
> 				}
> 				to{
> 					transform: rotate(180deg);
> 				}*/
> 				
> 				0%{
> 					background-color: yellow;
> 				}
> 				10%{
> 					background-color: green;
> 				}
> 				
> 				30%{
> 					transform: rotate(45deg);
> 				}
> 				60%{
> 					transform: scale(1.5);
> 				}
> 				
> 				100%{
> 					background-color: cyan;
> 				}
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div></div>
> 	</body>
> </html>
> ```

### 三、综合案例

#### 1.综合案例一：百度首页

> baidu.css文件：
>
> ```css
> /*取消所有标签默认的内外边距*/
> *{
> 	padding: 0px;
> 	margin: 0px;
> }
> 
> /*head部分*/
> #head{
> 	float: right;
> 	margin-top: 10px;
> 	margin-right: 10px;
> }
> /*设置超链接*/
> .headlink{
> 	color:black;
> 	font-size: 13px;
> 	margin: 5px;
> }
> /*更多产品*/
> .more{
> 	background-color: blue;
> 	color: white;
> 	text-decoration: none;
> 	margin-right: 5px;
> }
> 
> /*中间*/
> #middle{
> 	/*清除浮动：为了不影响后面标签的位置*/
> 	clear:right;
> 	
> 	text-align: center;
> 	
> 	position: absolute;
> 	top: 30px;
> 	
> 	width: 100%;
> }
> 
> /*输入框*/
> #key{
> 	width:30%;
> 	height: 30px;
> }
> /*百度一下*/
> #btn{
> 	width: 70px;
> 	height: 30px;
> 	background-color: blue;
> 	color: white;
> }
> 
> #footer{
> 	position: absolute;
> 	bottom: 0px;
> 	
> 	width: 100%;
> 	height: 200px;
> 	
> 	text-align: center;
> }
> 
> #footlink{
> 	margin: 20px;
> }
> 
> #footlink a{
> 	color: gray;
> 	font-size: 12px;
> }
> ```
>
> baidu.html文件
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<link href="css/baidu.css" type="text/css" rel="stylesheet"/>
> 	</head>
> 	<body>
> 		<!--上面部分-->
> 		<div id="head">
> 			<a href="#" class="headlink">新闻</a>
> 			<a href="#" class="headlink">hao123</a>
> 			<a href="#" class="headlink">视频</a>
> 			<a href="#" class="headlink">地图</a>
> 			<a href="#" class="headlink">贴吧</a>
> 			<a href="#" class="headlink">学术</a>
> 			<a href="#" class="headlink">登录</a>
> 			<a href="#" class="headlink">设置</a>
> 			<a href="#" class="more">更多产品</a>
> 		</div>
> 		
> 		
> 		<!--中间部分-->
> 		<div id="middle">
> 			<!--百度logo-->
> 			<img src="http://www.baidu.com/img/bd_logo1.png" />
> 			<div id="sub">
> 				<form action="#" method="get">
> 					<input type="text" name="keyword" id="key" />
> 					<!--<input type="submit" value="百度一下" />-->
> 					<button id="btn">百度一下</button>
> 				</form>
> 			</div>
> 		</div>
> 		
> 		
> 		<!--下面部分-->
> 		<div id="footer">
> 			<!--二维码-->
> 			<div>
> 				<img src="img/二维码.png" />
> 				<p>手机百度</p>
> 			</div>
> 			<!--=灰色的文字-->
> 			<div id="footlink">
> 				<a href="#">把百度设置为首页</a>
> 				<a href="#">关于百度</a>
> 				<a href="#">关于百度</a>
> 				<a href="#">关于百度</a>
> 				<br />
> 				<a href="#">关于百度</a>
> 				<a href="#">关于百度</a>
> 				<a href="#">关于百度</a>
> 			</div>
> 		</div>
> 	</body>
> </html>
> ```

#### 2.综合案例二：照片墙

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			#box{
> 				width: 80%;
> 				height: 800px;
> 				
> 				/*auto表示根据宽度自动适配外边距*/
> 				margin: 10px auto;
> 				
> 				background-color: orange;
> 			}
> 			
> 			/*图片的共性*/
> 			img{
> 				/*定位*/
> 				position:relative;
> 				
> 				width: 150px;
> 				height: 180px;
> 				
> 				border: 1px solid white;
> 				
> 				margin: 10px;
> 				
> 				/*过渡*/
> 				transition-duration: 2s;
> 				transition-property: transform;
> 
> 			}
> 			/*鼠标悬浮事件*/
> 			#box > img:hover{
> 				transform: scale(1.2) rotate(0deg);
> 				z-index:1;
> 			}
> 			
> 			/*没张图片的旋转角度的设置*/
> 			div img:nth-child(1){
> 				transform: rotate(15deg);
> 			}
> 			div img:nth-child(2){
> 				transform: rotate(-5deg);
> 			}
> 			div img:nth-child(3){
> 				transform: rotate(5deg);
> 			}
> 			div img:nth-child(4){
> 				transform: rotate(-15deg);
> 			}
> 			div img:nth-child(5){
> 				transform: rotate(20deg);
> 			}
> 			div img:nth-child(6){
> 				transform: rotate(-20deg);
> 			}
> 			div img:nth-child(7){
> 				transform: rotate(5deg);
> 			}
> 			div img:nth-child(8){
> 				transform: rotate(-15deg);
> 			}
> 			div img:nth-child(9){
> 				transform: rotate(15deg);
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<div id="box">
> 			<img src="img/photowall/pic1.jpg" />
> 			<img src="img/photowall/pic2.jpg" />
> 			<img src="img/photowall/pic3.jpg" />
> 			<img src="img/photowall/pic4.jpg" />
> 			<img src="img/photowall/pic5.jpg" />
> 			<img src="img/photowall/pic6.jpg" />
> 			<img src="img/photowall/pic7.jpg" />
> 			<img src="img/photowall/pic8.jpg" />
> 			<img src="img/photowall/pic9.jpg" />
> 		</div>
> 	</body>
> </html>
> ```

#### 3.综合案例三：时钟

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			#clock{
> 				width: 300px;
> 				height: 300px;
> 				border: solid 10px gray;
> 				/*削圆角*/
> 				border-radius: 50%;
> 				
> 				margin: 150px auto;
> 				
> 				position:relative;
> 			}
> 			
> 			/*设置所有线条的属性*/
> 			#clock .line{
> 				width: 5px;
> 				height: 300px;
> 				background-color: gray;
> 				position: absolute;
> 				left:50%;
> 			}
> 			/*设置每条线的旋转角度*/
> 			.line2{
> 				transform: rotate(30deg);
> 			}
> 			.line3{
> 				transform: rotate(60deg);
> 			}
> 			.line4{
> 				transform: rotate(90deg);
> 			}
> 			.line5{
> 				transform: rotate(120deg);
> 			}
> 			.line6{
> 				transform: rotate(150deg);
> 			}
> 			
> 			/*设置覆盖层*/
> 			#cover{
> 				width: 260px;
> 				height: 260px;
> 				border-radius: 50%;
> 				background-color: white;
> 				
> 				position: absolute;
> 				left:20px;
> 				top:20px;
> 			}
> 			
> 			/*设置针的样式*/
> 			#clock .zhen{
> 				position: absolute;
> 				/*水平方向：left center right
> 				 * 垂直方向：top center bottom
> 				 */
> 				transform-origin: center bottom;
> 			}
> 			
> 			/*设置秒针*/
> 			#clock .seconds{
> 				width: 2px;
> 				height:140px;
> 				background-color: blue;
> 				left:151px;
> 				top:10px;
> 					
> 				animation: circle 60s steps(60) infinite;
> 			}
> 			/*设置分针*/
> 			#clock .minute{
> 				width: 4px;
> 				height:120px;
> 				background-color: red;
> 				left:150px;
> 				top:30px;
> 					
> 				animation: circle 3600s infinite linear;
> 			}
> 			
> 			/*设置时针*/
> 			#clock .hour{
> 				width: 6px;
> 				height:100px;
> 				background-color: orange;
> 				left:149px;
> 				top:50px;
> 					
> 				animation: circle 43200s infinite linear;
> 			}
> 			
> 			@keyframes circle{
> 				from{transform: rotate(0deg);}
> 				to{transform: rotate(360deg);}
> 			}
> 			
> 			/*圆心*/
> 			#dotted{
> 				width: 20px;
> 				height: 20px;
> 				background-color: gray;
> 				border-radius: 50%;
> 				position: absolute;
> 				left:140px;
> 				top:140px;	
> 			}
> 				
> 		</style>
> 	</head>
> 	<body>
> 		<!--整体-->
> 		<div id="clock">
> 			<!--刻度-->
> 			<div class="line line1"></div>
> 			<div class="line line2"></div>
> 			<div class="line line3"></div>
> 			<div class="line line4"></div>
> 			<div class="line line5"></div>
> 			<div class="line line6"></div>
> 			<!--覆盖层-->
> 			<div id="cover"></div>
> 			<!--指针-->
> 			<div class="zhen hour"></div>
> 			<div class="zhen minute"></div>
> 			<div class="zhen seconds"></div>
> 			<!--圆心-->
> 			<div id="dotted"></div>
> 		</div>
> 	</body>
> </html>
> ```

### html和css的案例：卧龙首页

> WLHome.css文件
>
> ```html
> *{
> 	margin: 0px;
> 	padding: 0px;
> }
> 
> /*设置头部*/
> #head{
> 	width: 100%;
> 	height: 50px;
> }
> 
> /*调整logo图*/
> #head > img{
> 	margin: 10px;
> }
> 
> /*设置搜索框和搜偶按钮*/
> #search{
> 	float: right;
> 	margin: 10px;
> }
> #search input{
> 	height: 25px;
> 	float: left;
> }
> 
> #search button{
> 	float: left;
> 	border: 0px;
> }
> 
> /*导航*/
> #nav{
> 	width: 100%;
> 	height: 50px;
> 	background-color: black;
> }
> #nav div{
> 	float: left;
> 	color: white;
> 	height: 100%;
> }
> 
> .info{
> 	width: 19.8%;
> 	text-align: center;
> 	line-height: 50px;
> }
> .line{
> 	width:0.25%;
> 	background-color: white;
> }
> 
> #image{
> 	width: 100%;
> }
> 
> #image > img{
> 	width: 100%;
> 	height: 100%;
> }
> 
> #forth{
> 	width: 100%;
> 	height: 150px;
> }
> 
> /*将新闻资讯，人才介绍三部分内容横向排列*/
> #forth > div{
> 	float: left;
> 	/*margin-left: 5px;*/
> 	height: 100%;
> }
> 
> #forth li,#forth p{
> 	font-size: 12px;
> 	color: gray;
> }
> 
> #news{
> 	width: 40%;
> }
> 
> #detail,#invite{
> 	width: 30%;
> }
> 
> #market{
> 	width: 100%;
> }
> 
> #market li{
> 	display: inline-block;
> 	width: 23%;
> }
> ```
>
> WLHome.html文件
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<link href="css/WlHome.css" type="text/css" rel="stylesheet"/>
> 	</head>
> 	<body>
> 		<div id="box">
> 			<!--头部-->
> 			<div id="head">
> 				<!--左边logo-->
> 				<img src="img/WLImages/logo_01.jpg" />
> 				<!--右边搜索框-->
> 				<div id="search">
> 					<form>
> 						<input type="text" name="content" placeholder="请输入内容" />
> 						<button><img src="img/WLImages/button.jpg"/></button>
> 					</form>
> 				</div>
> 			</div>
> 			
> 			<!--导航-->
> 			<div id="nav">
> 				<div class="info"><a>集团介绍</a></div>
> 				<div class="line"></div>
> 				<div class="info"><a>集团介绍</a></div>
> 				<div class="line"></div>
> 				<div class="info"><a>集团介绍</a></div>
> 				<div class="line"></div>
> 				<div class="info"><a>集团介绍</a></div>
> 				<div class="line"></div>
> 				<div class="info"><a>集团介绍</a></div>
> 			</div>
> 			
> 			<!--顶部大图-->
> 			<div id="image"><img src="img/WLImages/banner.jpg"/></div>
> 			
> 			<!--新闻资讯，人才介绍，人才招聘-->
> 			<div id="forth">
> 				<!--新闻资讯-->
> 				<div id="news">
> 					<h3>新闻资讯</h3>
> 					<ul>
> 						<li>fwhuerghwjrghjergh</li>
> 						<li>fwhuerghwjrghjergh</li>
> 						<li>fwhuerghwjrghjergh</li>
> 						<li>fwhuerghwjrghjergh</li>
> 						<li>fwhuerghwjrghjergh</li>
> 					</ul>
> 				</div>
> 				<!--卧龙介绍-->
> 				<div id="detail">
> 					<h3>卧龙介绍</h3>
> 					<p>新闻资讯，人才介绍</p>
> 					<p>新闻资讯，人才介绍</p>
> 				</div>
> 				<!--人才招聘-->
> 				<div id="invite">
> 					<h3>人才招聘</h3>
> 					<p>人才招聘人才招聘</p>
> 					<img src="img/WLImages/flower.jpg" />
> 					<button>more</button>
> 				</div>
> 			</div>
> 			
> 			<!--卧龙市场
> 			-->
> 			<div id="market">
> 				<h3>卧龙市场</h3>
> 				<ul>
> 					<li>
> 						<img src="img/WLImages/img02.jpg" />
> 						<p>培养一流的人才</p>
> 					</li>
> 					<li>
> 						<img src="img/WLImages/img02.jpg" />
> 						<p>培养一流的人才</p>
> 					</li>
> 					<li>
> 						<img src="img/WLImages/img02.jpg" />
> 						<p>培养一流的人才</p>
> 					</li>
> 					<li>
> 						<img src="img/WLImages/img02.jpg" />
> 						<p>培养一流的人才</p>
> 					</li>
> 				</ul>
> 			</div>
> 		</div>
> 	</body>
> </html>
> ```

### 