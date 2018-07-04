> html---->css--->javascript---->jQuery----->ajax----->bootstrap
>
> 1.是什么
>
> 2.该怎么使用
>
> 3.有什么作用

### 一、网页开发基础知识

> 网页文件是使用html进行书写
>
> 产生一个网页文件，文本文档，Hbuilder，DreamWeaver,eclipse
>
> **网页主要由三个部分组成：结构，表现，行为**
>
> ​	结构：网页的结构和内容【一个网页包括标题，正文段落或者列表】-----》html
>
> ​	表现：设定网页的样式【字号，字体，颜色等】--------》css
>
> ​	行为：控制网页的行为【网页可以变化，可以和读者进行交互】-------》javascript
>
> 总之：html决定了网页是什么，css决定了网页是什么样式，javascript决定了网页能做什么
>
> 其中，前期html可以同时承担结构和表现的双重任务
>
> 一个网站从无到有的过程：
>
> 客户/产品经理提出来的需求-------》设计师进行设计-----》设计师和程序员合作完成------》测试人员----》程序员发布

### 二、html简介

#### 1.概念

> html，HyperText Markup Language,**超文本标记语言**
>
> 超文本：超出文本的范围
>
> 标记：html中所有的操作都是通过标记【标签】实现的
>
> html1 ~ html5:是最基础的网页语言，是解释型和编译型的语言

#### 2.第一个html程序

> 注意：
>
> a.文件格式为xx.html或者xxx.htm
>
> b.这是<font size="5" color="red">第一个html程序</font>,其中，font被称为标签，size和color被称为属性
>
> ```html
> <html>
> 	<head>
> 		<title>
> 			网页标题
> 		</title>
> 	</head>	
> 	<body>
> 		这是<font size="5" color="red">第一个html程序</font>
> 		<br/>
> 		和Python&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;的区别
> 	</body>	
> 
> </html>
> ```

#### 3.html的书写规范

> ```html
> a.一个html文件包含一个开始标签和结束标签：<html></html>
> b.html标签中包含两部分内容：
> 	<head></head>:用来设置html页面的属性和配置信息
> 	<body></body>:显示在网页中的内容
> c.在head标签中包含两部分内容
> 	<title></tilte>:设置网页标题
> 	<meta charset="utf-8">:**设置网页的编码格式**
> d.html中的标签分为两种：一类开始标签和结束标签，另外一类只有开始标签或者只有结束标签
> e.html中的标签不区分大小写
> ```
>
> ```html
> <!--文档类型的声明-->
> <!DOCTYPE html>
> <html>
> 	<!--设置html页面的属性和配置信息-->
> 	<head>
> 		<!--设置当前文件的编码格式-->
> 		<meta charset="utf-8" />
> 		<!--设置当前文件的标题-->
> 		<title>网页标题</title>
> 	</head>
> 	<body>
> 		<!--需要显示在页面上的内容-->
> 		hello html
> 	</body>
> </html>
> <!--
> 标签之间的关系
> 	a.父子关系：直接的包含关系
> 	b.兄弟关系：拥有同一个父标签的标签【平级】
> 	c.先辈后辈关系：隔代关系，父子关系
> html标签之间是可以进行嵌套的
> -->
> ```
>
> html文件的命名规则：
>
> ​	a.可以由数字，字母，下划线，**$**
>
> ​	b.不能以数字开头，不要出现空格
>
> ​	c.大驼峰命名法

#### 4.html的操作思想

> 封装：一个标签就相当于是一个容器，想要修改容器内数据的样式，只需要修改容器属性的值，就可以实现修改内部数据的样式

### 三、html常用的标签

#### 1.文字标签和段落标签

##### 1.1文字标签

> ```html
> <font></font>
> ```
>
> 属性：
>
> ​	size：文字的大小，**取值范围为1~7，数值超过7之后仍然是7的大小**
>
> ​	color:文字的颜色，有两种方式表示
>
> ​		方式一：英文单词【red,green....】
>
> ​		方式二:采用十六进制表示
>
> ​			举例：#123456，每两位表示一种颜色，分别表示三原色，是RGB
>
> ​			其中：#000000黑色   #FFFFFF白色
>
> ​		方式三：**rgb(r,g,b)     rgba()   参数的取值范围为0~255**
>
> ​			a----》**alpha:透明度，取值范围为0~1**
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<font size="4" color="#56abcd">hello html</font>
> 		<font size="4" color="cyan">hello html</font>
> 	</body>
> </html>
> ```

##### 1.2段落标签

> ```html
> <p></p>
> ```
>
> **注意：**
>
> **​	a.不同的p标签之间默认可以换行**
>
> **	b.在同一个p的内部，多条数据之间可以换行**
>
> ​        **c.如果要设置段落中文字的样式，借助于font标签**
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<p>第一个段落</p>
> 		<p>第一个段落</p>
> 		<p>第一个段落</p>
> 		<p>第一个段落</p>
> 		
> 		<!--p结合font标签的使用-->
> 		<p>
> 			<font size="5" color="green">贾乃亮</font>与李小璐是在某个饭局上认识，随后他就对女方一见钟情，锲而不舍展开疯狂追求。李小璐曾在某访谈节目中透露，当时贾乃亮为了追求自己，还特别去打了一串与自己一样的耳洞，而且感染化脓，就只是为了引起她的注意，还有一次是李小璐发烧生病，贾乃亮衣不解带的守在身边照顾了5天5夜，连头都来不及洗，就是一直陪在自己身边。但是这也没让李小璐接受对方的追求，直到快1年了，有一次她看到贾乃亮喝醉，在自己面前委屈痛哭，才惊觉对方是对自己是认真的，才点头同意交往
> 		</p>
> 	</body>
> </html>
> ```

##### 1.3和字体有关的其他标签【了解】

> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<!--删除标签-->
> 		<s>hello</s>
> 		<del>hello</del>
> 		
> 		<!--加粗标签-->
> 		<b>hello</b>
> 		<strong>hello</strong>
> 		
> 		<!--斜体标签-->
> 		<!--只是一种字体，意大利体-->
> 		<i>hello</i>   
> 		<!--使得文本倾斜一定的角度-->
> 		<em>hello</em>
> 		
> 		<!--下划线标签-->
> 		<u>hello</u>
> 		<ins>hello</ins>
> 		
> 		<!--上标和下标-->
> 		<!--
> 			log2
> 		-->
> 		<sup>hello</sup>
> 		<sub>hello</sub>
> 		
> 		2<sup>5</sup>
> 		log<sub>2</sub>
> 			
> 	</body>
> </html>
> ```

#### 2.标题标签

> <hn></hn>
>
> n的取值范围：1~6
>
> 说明：数字越大，则表示的标题的字号越小
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
> 		<h1>千锋教育</h1>
> 		<h2>千锋教育</h2>
> 		<h3>千锋教育</h3>
> 		<h4>千锋教育</h4>
> 		<h5>千锋教育</h5>
> 		<h6>千锋教育</h6>
> 		
> 	</body>
> </html>
> ```

#### 3.水平线标签、换行标签和特殊字符

##### 3.1水平线标签和换行标签

> <hr />
>
> ​	size:水平线的高度  color:水平线的颜色
>
> <br />
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
> 		<hr />
> 		<hr size="3" color="blue" />
> 		
> 		第一段
> 		<br />
> 		第二段
> 		
> 		<!--特殊字符-->
> 		<!--<html>是网页的开始-->
> 		&lt;html&gt;是网页的开始
> 		
> 		html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;hello
> 		
> 		3&times;2 = 6
> 		6&divide;2 = 3
> 	</body>
> </html>
> ```

##### 3.2特殊字符

> ```
> &quot;  双引号
> &amp;   &符号
> &copy;	版权
> &reg;	注册商标
> ```
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
> 		
> 		<!--特殊字符-->
> 		<!--<html>是网页的开始-->
> 		&lt;html&gt;是网页的开始
> 		
> 		html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;hello
> 		
> 		3&times;2 = 6
> 		6&divide;2 = 3
> 	</body>
> </html>
> ```

#### 4.图像标签

##### 4.1图像标签的使用

> <img />
>
> 属性：
>
> ​	src:图片的路径
>
> ​		网络资源：直接赋值网址即可
>
> ​		本地资源；图片的本地路径【绝对路径和相对路径】
>
> ​	width：图片显示的宽度
>
> ​	height：图片显示的高度
>
> ​		单位：px【像素】      
>
> ​		百分比 ：50%
>
> ​	alt:图片上的文字提示【如果图片路径不存在，显示该文本】
>
> ​	title：鼠标悬浮标题，注意和alt之间的区别
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
> 		<!--直接加载图片，如果设置大小，则默认显示的是图片本身的大小-->
> 		<!--加载本地图片-->
> 		<img src="img/背景1.jpg" width="100px" height="100px"/>
> 		<!--加载网络图片-->
> 		<img src="http://www.baidu.com/img/bd_logo1.png" />
> 		
> 		
> 		<!--width和height的使用-->
> 		<img src="img/背景1.jpg" width="100px" height="100px"/>
> 		<!--
> 			图片的比例 a:b = w:h
> 			设置了w 
> 			h = w * b / a
> 		-->
> 		<br />
> 		<!--按照比例缩放，参照比例是浏览的宽和高的比例-->
> 		<img src="img/背景1.jpg" width="100%" height="100%"/>
> 		
> 		<br />
> 		<!--alt的使用-->
> 		<img src="img/背景.jpg" width="100px" height="100px" alt="图片未记载"/>
> 		
> 		<br />
> 		<!--title的使用-->
> 		<img src="img/背景1.jpg" width="100px" height="100px" title="桌面壁纸"/>
> 	</body>
> </html>
> ```

##### 4.2相对路径和绝对路径

> 相对路径：表示一个文件相对于另外一个文件的位置，重点在于找到一个参照物
>
> 绝对路径：
>
> ​	当前html文件和图片文件路径之间的关系
>
> ​	a.在同一级目录下
>
> ​	b.html文件和图片的上一级目录在同一级目录下
>
> ​	c.图片和html文件的上一级目录在同一级目录下
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
> 		<!--相对路径-->
> 		<!--形式一:html文件和图片是平级-->
> 		<img src="背景1.jpg" />
> 		
> 		<!--形式二：html文件和图片的上一级目录在同一级目录下-->
> 		<img src="img/背景1.jpg"/>
>       
> 		<!--形式三：../代表上一级目录，如果有多级目录：../../../-->
> 		<img src="../背景1.jpg" />
> 		<!--
> 			src="../img/背景1.jpg"
> 		-->
> 	</body>
> </html>	
> ```

#### 5.块标签

> <pre></pre>：其中的内容按照原样输出
>
> <div></div>:会自动换行，在css中使用，主要用于分模块布局
>
> <span></span>:不会自动换行【注册用户时错误后面的提示】
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
> 		<p>
> 			def text():
> 				pass
> 		</p>
> 		<!--可以将其中的数据按照原样输出-->
> 		<pre>
> 			def text():
> 				pass
> 		</pre>
> 		
> 		<div>562745</div>
> 		<div>562745</div>
> 		<div>562745</div>
> 		<div>562745</div>
> 		<div>562745</div>
> 		
> 		<span>hfjsfjs</span>
> 		<span>hfjsfjs</span>
> 		<span>hfjsfjs</span>
> 		<span>hfjsfjs</span>
> 		<span>hfjsfjs</span>
> 	</body>
> </html>
> ```

#### 6.列表标签

##### 6.1自定义列表/解释型列表

> <dl></dl>:表示列表的范围，角色为父标签
>
> ​	<dt></dt>:上层内容，角色为子标签
>
> ​	<dd></dd>:下层内容，角色为子标签
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
> 		<!--1.自定义列表-->
> 		<dl>
> 			<!--上层内容-->
> 			<dt>千锋教育</dt>
> 			<!--下层内容-->
> 			<dd>财务部</dd>
> 			<dd>人事部</dd>
> 			<dd>教学部</dd>
> 		</dl>
> 	</body>
> </html>
> ```

##### 6.2有序列表

> <ol></ol>:表示有序列表的范围。角色为父标签
>
> ​	<li></li>:具体内容，角色为子标签
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
> 		
> 		<!--2.有序列表-->
> 		<!--修改有序列表的样式，设置type属性，取值1，a,A,i,I,默认为1-->
> 		<ol type="1">
> 			<li>千锋教育</li>
> 			<li>财务部</li>
> 			<li>人事部</li>
> 			<li>教学部</li>
> 		</ol>
> 		
> 		<ol start="2" type="1">
> 			<li>千锋教育</li>
> 			<li>财务部</li>
> 			<li>人事部</li>
> 			<li>教学部</li>
> 		</ol>
> 	</body>
> </html>
> ```

##### 6.3无序列表

> <ul></ul>:表示无序列表的范围，角色为父标签
>
> ​	<li></li>:具体内容，角色为子标签
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
> 		<!--3.无序列表-->
> 		<!--通过设置type修改无序列表的样式，circle表示空心圆，disc表示实心圆，square表示空心方框，默认为disc-->
> 		<ul type="square">
> 			<li>千锋教育</li>
> 			<li>财务部</li>
> 			<li>人事部</li>
> 			<li>教学部</li>
> 		</ul>
> 	</body>
> </html>
> ```

#### 7.表格标签

> 可以对数据进行格式化，使得数据的显示更加条理化
>
> <table></table>:表示表格的范围，角色是父标签
>
> ​	<tr></tr>:表示行，角色是子标签
>
> ​		<td></td>:表示列【单元格】，角色：是tr的子标签
>
> <caption></caption>:设置表格的标题
>
> 属性：
>
> ​	border:表格边框的线条宽度
>
> ​	bordercolor:边框的颜色
>
> ​	cellspacing:单元格之间的间隔
>
> ​	width:表格或者单元格的宽度
>
> ​	height:表格或者单元格的高度
>
> ​	align:对齐方式，取值为left，center，right，默认向左对齐
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
> 		<!--需求：实现一个四行三列的表格-->
> 		<table border="1px" bordercolor="blue" cellspacing="3px" width="300px" height="500px">
> 			<tr align="center">
> 				<td>姓名</td>
> 				<td>年龄</td>
> 				<td>性别</td>
> 			</tr>
> 			<tr>
> 				<td align="right">张三</td>
> 				<td>18</td>
> 				<td>男</td>
> 			</tr>
> 			<tr>
> 				<td>李四</td>
> 				<td>20</td>
> 				<td>女</td>
> 			</tr>
> 			<tr>
> 				<!--注意：th和td之间的区别：默认居中显示，加粗字体-->
> 				<th>王麻子</th>
> 				<td>10</td>
> 				<td>不男不女</td>
> 			</tr>
> 		</table>
> 		
> 		<!--单元格的合并-->
> 		<table border="1px" bordercolor="blue" cellspacing="3px" width="300px" height="500px">
> 			<tr align="center">
> 				<!--colspan:合并列，将n列合并为一列-->
> 				<td colspan="3">人员信息</td>
> 			</tr>
> 			<tr>
> 				<td align="right">张三</td>
> 				<td>18</td>
> 				<td>男</td>
> 			</tr>
> 			<tr>
> 				<td>李四</td>
> 				<td>20</td>
> 				<td>女</td>
> 			</tr>
> 			<tr>
> 				<!--注意：th和td之间的区别：默认居中显示，加粗字体-->
> 				<th>王麻子</th>
> 				<td>10</td>
> 				<td>不男不女</td>
> 			</tr>
> 		</table>
> 		
> 		<table border="1px" bordercolor="blue" cellspacing="3px" width="300px" height="500px">
> 			<tr align="center">
> 				<td>赵四</td>
> 				<td>33</td>
> 				<!--rowspan：合并行-->
> 				<td rowspan="4">男</td>
> 			</tr>
> 			<tr>
> 				<td align="right">张三</td>
> 				<td>18</td>
> 				
> 			</tr>
> 			<tr>
> 				<td>李四</td>
> 				<td>20</td>
> 				
> 			</tr>
> 			<tr>
> 				<!--注意：th和td之间的区别：默认居中显示，加粗字体-->
> 				<th>王麻子</th>
> 				<td>10</td>
> 			</tr>
> 		</table>
> 	</body>
> </html>
> ```

### 一、上堂回顾

> 1.网页开发的基础知识
>
> ​	组成：结构，表现，行为
>
> ​		html，css，javascript
>
> 2.html简介
>
> ​	规范：
>
> ​	操作思想：封装
> 3.html中常用的标签
>
> ​	font：设置字体，size，color
>
> ​	p：段落
>
> ​	h标签：标题
>
> ​	hr  :size，color
>
> ​	br:换行
>
> ​	特殊字符【字符实体】：&nbsp;
>
> ​	img:src,width,height,alt,title
>
> ​		相对路径的使用：../
>
> ​	块标签：pre   div  span
>
> ​	列表标签：有序【ol】，无序【ul】   li
>
> ​	表格：table   tr   td
>
> ​	           colspan,rowspan

### 二、html中的常用标签

#### 8.超链接标签

##### 8.1简单使用

> <a></a>
>
> 属性：
>
> ​	href：表示需要链接到的资源路径
>
> ​		本地资源：注意相对路径
>
> ​		网络资源：直接加载
>
> ​	target：设置打开的方式，默认在当前窗口中打开
>
> ​		_blank:在一个新的窗口打开
>
> ​		_self:在当前窗口打开
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 	</head>
> 	<body>
> 		<!--超链接的作用：通过点击，然后 进行跳转到指定资源-->
> 		<!--1.链接本地地址-->
> 		<!--target默认为为_self-->
> 		<a href="text.html">我是一个超链接</a>
> 		<a href="text.html" target="_self">我是一个超链接~~~~</a>
> 		
> 		<br />
> 		<!--_blank表示新打开一个窗口，返回按钮消失-->
> 		<a href="text.html" target="_blank">我是一个超链接111</a>
> 		
> 		<!--2.相对路径-->
> 		<a href="code/check.html">点击</a>
> 		
> 		<!--3.链接网络地址-->
> 		<a href="http://www.baidu.com">百度一下</a>
> 		
> 		<!--4.让图片有超链接的效果-->
> 		<a href="text.html">
> 			<img src="img/背景1.jpg" width="50px" height="50px"/>
> 		</a>
> 		
> 		<!--5.让超链接没有点击效果-->
> 		<!--如果超链接不需要连接到任何地方，设置一个占位符#-->
> 		<a href="#">点点点</a>
> 		
> 		<a href="javascript:void(0)">不链接</a>
> 		
> 	</body>
> </html>	
> ```

##### 8.2定位资源

> 1>回到顶部
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title>超链接的定位资源</title>
> 	</head>
> 	<body>
> 		<!--回到顶部-->
> 		<p>
> 			据台湾媒体报道，演员贾乃亮近日深陷婚变风波，老婆李小璐被拍到与饶舌歌手勾手、共度一夜的画面，他6日发出长文回应此事，内容却被网友解读为是在默认“被戴绿帽”，事情越演越烈，两人过去在录节目的互动，以及放闪画面也一一被翻出，网友发现其实贾乃亮真的非常爱李小璐，向对方求了3次婚，而且还会为对方下厨等。
>     贾乃亮与李小璐是在某个饭局上认识，随后他就对女方一见钟情，锲而不舍展开疯狂追求。李小璐曾在某访谈节目中透露，当时贾乃亮为了追求自己，还特别去打了一串与自己一样的耳洞，而且感染化脓，就只是为了引起她的注意，还有一次是李小璐发烧生病，贾乃亮衣不解带的守在身边照顾了5天5夜，连头都来不及洗，就是一直陪在自己身边。但是这也没让李小璐接受对方的追求，直到快1年了，有一次她看到贾乃亮喝醉，在自己面前委屈痛哭，才惊觉对方是对自己是认真的，才点头同意交往。
> 		</p>
> 		<!--回到顶部-->
> 		<p>
> 			据台湾媒体报道，演员贾乃亮近日深陷婚变风波，老婆李小璐被拍到与饶舌歌手勾手、共度一夜的画面，他6日发出长文回应此事，内容却被网友解读为是在默认“被戴绿帽”，事情越演越烈，两人过去在录节目的互动，以及放闪画面也一一被翻出，网友发现其实贾乃亮真的非常爱李小璐，向对方求了3次婚，而且还会为对方下厨等。
>     贾乃亮与李小璐是在某个饭局上认识，随后他就对女方一见钟情，锲而不舍展开疯狂追求。李小璐曾在某访谈节目中透露，当时贾乃亮为了追求自己，还特别去打了一串与自己一样的耳洞，而且感染化脓，就只是为了引起她的注意，还有一次是李小璐发烧生病，贾乃亮衣不解带的守在身边照顾了5天5夜，连头都来不及洗，就是一直陪在自己身边。但是这也没让李小璐接受对方的追求，直到快1年了，有一次她看到贾乃亮喝醉，在自己面前委屈痛哭，才惊觉对方是对自己是认真的，才点头同意交往。
> 		</p>
> 		<!--回到顶部-->
> 		<p>
> 			据台湾媒体报道，演员贾乃亮近日深陷婚变风波，老婆李小璐被拍到与饶舌歌手勾手、共度一夜的画面，他6日发出长文回应此事，内容却被网友解读为是在默认“被戴绿帽”，事情越演越烈，两人过去在录节目的互动，以及放闪画面也一一被翻出，网友发现其实贾乃亮真的非常爱李小璐，向对方求了3次婚，而且还会为对方下厨等。
>     贾乃亮与李小璐是在某个饭局上认识，随后他就对女方一见钟情，锲而不舍展开疯狂追求。李小璐曾在某访谈节目中透露，当时贾乃亮为了追求自己，还特别去打了一串与自己一样的耳洞，而且感染化脓，就只是为了引起她的注意，还有一次是李小璐发烧生病，贾乃亮衣不解带的守在身边照顾了5天5夜，连头都来不及洗，就是一直陪在自己身边。但是这也没让李小璐接受对方的追求，直到快1年了，有一次她看到贾乃亮喝醉，在自己面前委屈痛哭，才惊觉对方是对自己是认真的，才点头同意交往。
> 		</p>
> 		<!--回到顶部-->
> 		<p>
> 			据台湾媒体报道，演员贾乃亮近日深陷婚变风波，老婆李小璐被拍到与饶舌歌手勾手、共度一夜的画面，他6日发出长文回应此事，内容却被网友解读为是在默认“被戴绿帽”，事情越演越烈，两人过去在录节目的互动，以及放闪画面也一一被翻出，网友发现其实贾乃亮真的非常爱李小璐，向对方求了3次婚，而且还会为对方下厨等。
>     贾乃亮与李小璐是在某个饭局上认识，随后他就对女方一见钟情，锲而不舍展开疯狂追求。李小璐曾在某访谈节目中透露，当时贾乃亮为了追求自己，还特别去打了一串与自己一样的耳洞，而且感染化脓，就只是为了引起她的注意，还有一次是李小璐发烧生病，贾乃亮衣不解带的守在身边照顾了5天5夜，连头都来不及洗，就是一直陪在自己身边。但是这也没让李小璐接受对方的追求，直到快1年了，有一次她看到贾乃亮喝醉，在自己面前委屈痛哭，才惊觉对方是对自己是认真的，才点头同意交往。
> 		</p>
> 		
> 		<!--在当前页面中做超链接-->
> 		<a href="#top">回到顶部</a>
> 		
> 	</body>
> </html>
> ```
>
> 2>定位到页面的具体段落
>
> 代码演示：
>
> pageInfo.html
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<!--html中所有的标签都有id,style,class等属性-->
> 		<p id="p1" style="height: 1000px; background-color: red;">第一段落</p>
> 		<p id="p2" style="height: 1000px; background-color: blue;">第二段落</p>
> 		<p id="p3" style="height: 1000px; background-color: purple;">第三段落</p>
> 		<p id="p4" style="height: 1000px; background-color: cyan;">第四段落</p>
> 	</body>
> </html>
> ```
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title>超链接标签的定位资源</title>
> 	</head>
> 	<body>
> 		<a href="pageInfo.html#p1">第一段</a>
> 		<a href="pageInfo.html#p2">第er段</a>
> 		<a href="pageInfo.html#p3">第三段</a>
> 		<a href="pageInfo.html#p4">第四段</a>
> 	</body>
> </html>
> ```

#### 9.音视频标签

##### 9.1音频

> html5新增，可以加载mp3,wav
>
> <audio></audio>
>
> 属性：
>
> ​	src：设置需要加载的音频的资源路径
>
> ​	autoplay:自动加载
>
> ​	controls:显示进度条
>
> ​	loop：循环播放

##### 9.2视频

> <video></video>
>
> 可以加载mp4,wav等
>
> 属性：
>
> ​	src：设置需要加载的音频的资源路径
>
> ​	autoplay:自动加载
>
> ​	controls:显示进度条
>
> ​	loop：循环播放

#### 10.表单标签【重点】

> 作用：可以提交不同类型的数据到指定服务器
>
> 标签：
>
> ​	<form></form>:表示表单的范围【父标签】
>
> ​	这个标签主要是用于采集用户信息,分为：表单标签、表单域、表单按钮	
>
> ​	属性：
>
> ​		action：提交的位置
>
> ​		method：提交的方式【get，post】
>
> ​		enctype:很少用，做文件提交的时候使用
>
> ​	子标签：
>
> ​		<input  />:表示输入项【子标签】
>
> ​			普通输入项：type="text"
>
> ​			密码输入项：type="password"
>
> ​			单项输入项：type="radio"
>
> ​			多项输入项：type="checkbox"
>
> ​			文件输入项：type="file"
>
> ​			邮件输入项：type="email"
>
> ​			颜色输入项：type="color"
>
> ​			日期输入项：type="date"
>
> ​			进度条输入项：type="range"
>
> ​			提交按钮：type="submit"
>
> ​			重置按钮：type="reset"
>
> ​		<select></select>:下拉菜单
>
> ​			<option></option>:下拉菜单中的选项
>
> ​		<textarea></textarea>:文本域【可以输入多行】
>
> 初始状态
>
> http://127.0.0.1:8020/Day2Code/text.html
>
> 添加name属性
>
> http://127.0.0.1:8020/Day2Code/text.html?phoneNum=525266&username=sbhs&pwd=bsnbs&sex=on&hobby=on&hobby=on&headImage=&birth=1990&des=bsefhrtjnety
>
> 添加value属性
>
> http://127.0.0.1:8020/Day2Code/text.html?phoneNum=6374&username=twerg&pwd=gwer&sex=female&hobby=l&hobby=p&headImage=&birth=1989&des=hthrtj
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
> 		<!--在表单标签中，每个标签都有value【值】，name【提交给服务器，方便服务器进行区分是哪种数据】属性-->
> 		<!--placeholder：未输入之前的提示文本，不影响正常的输入-->
> 			
> 		<!--action表示提交到的位置，method表示提交的方式-->
> 		<form action="text.html" method="get">
> 			<!--普通输入项-->
> 			手机号码：<input type="text" name="phoneNum"/><br />
> 			姓名：<input type="text" name="username" /><br />
> 			<!--密码输入项-->
> 			创建密码：<input type="password" name="pwd" /><br />
> 			<!--单项输入项-->
> 			性别：<input type="radio" name="sex" value="male"/>男
> 				 <input type="radio" name="sex" value="female"/>女
> 			<br />
> 			<!--多项输入项-->
> 			爱好：<input type="checkbox" name="hobby" value="l"/>篮球
> 				 <input type="checkbox" name="hobby" value="p"/>排球
> 				 <input type="checkbox" name="hobby" value="z"/>足球
> 				 <input type="checkbox" name="hobby" value="y"/>羽毛球
> 			<br />
> 			<!--文件输入项-->
> 			上传头像：<input type="file" name="headImage" />
> 			<br />
> 			<!--下拉菜单-->
> 			出生年月：<select name="birth">
> 						<option>1988</option>
> 						<option>1989</option>
> 						<option>1990</option>
> 						<option>1991</option>
> 						<option>1992</option>
> 					</select>
> 			<br />
> 			<!--文本域-->
> 			自我评价：<textarea cols="30" rows="4" name="des"></textarea>
> 			<br />
> 			
> 			<!--了解-->
> 			<!--邮箱-->
> 			<!--placeholder：提示-->
> 			邮箱：<input type="email" placeholder="请输入邮箱" />
> 			颜色：<input type="color" />
> 			日期：<input type="date" />
> 			<br />
> 			进度条：<input type="range" min="0"  max="100" value="10" />
> 			隐藏域：<input type="hidden" />
> 			
> 			<!--按钮-->
> 			<!--value：设置按钮上的文字-->
> 			<!--普通按钮，没有任何功能-->
> 			<input type="button" value="点击"/>
> 			<!--重置按钮：将整个表单的内容恢复到初始状态-->
> 			<input type="reset" value="reset"/>
> 			<!--提交按钮：将整个表单的内容提交到指定服务器-->
> 			<input type="submit" value="submit"/>
> 		</form>
> 	</body>
> </html>
> ```
>
> 两种提交方式之间的区别【面试题】
>
> ​	a.get提交数据地址栏中会出现所有的数据，post不会携带【请求体】
>
> ​	b.get请求安全级别较低，post相对较高
>
> ​	c.get请求传输数据的效率较高，post相对较低
>
> ​	d.get请求对数据的大小有限制，但是post没有
>
> 练习：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<h3>还没有千锋教育账号？</h3>
> 		<form>
> 			<table width="100%">
> 				<tr>
> 					<td align="right">电子邮箱</td>
> 					<td>
> 						<input type="email" name="email" />
> 					</td>
> 				</tr>
> 				<tr>
> 					<td>&nbsp;</td>
> 					<td>
> 						你可以使用<a href="#">电子邮箱</a>或者<a href="#">手机号</a>注册
> 					</td>
> 				</tr>
> 				<tr>
> 					<td align="right">性别</td>
> 					<td>
> 						<input type="radio" name="sex" value="nan" />男
> 						<input type="radio" name="sex" value="nv" />女
> 					</td>
> 				</tr>
> 				<tr>
> 					<td align="right">出生年月</td>
> 					<td>
> 						<select>
> 							<option></option>
> 							<option></option>
> 							<option></option>
> 							<option></option>
> 						</select>年
> 						<select>
> 							<option></option>
> 							<option></option>
> 							<option></option>
> 							<option></option>
> 						</select>月
> 						<select><option></option>
> 							<option></option>
> 							<option></option>
> 							<option></option>
> 						</select>日
> 					</td>
> 				</tr>
> 				<tr></tr>
> 				<tr></tr>
> 				<tr></tr>
> 			</table>
> 		</form>
> 	</body>
> </html>
> ```

#### 11.头标签

> 头标签：head
>
> <title></title>:设置网页的标题
>
> <base></base>:设置超链接的基本位置，可以统一打开的方式
>
> <mate />:设置当前页面的一些信息
>
> ​	charset：字符集【编码格式】
>
> ​	name：关键字
>
> ​	content：内容
>
> <link />:在css中用于引入外部css文件	
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		
> 		<title>网页的标题</title>
> 		
> 		<!--早期的搜索引擎，通过指定的关键字进行搜索-->
> 		<meta charset="utf-8" name="keywords" content="千锋,it" />
> 		
> 		<!--当前页面经过3秒之后跳转到url指定的页面-->
> 		<!--<meta http-equiv="refresh" content="3;url=http://www.baidu.com"/>-->
> 		
> 		<!--设置当前页面中所有的超链接都按照指定的方式打开页面-->
> 		<base target="_blank" />
> 		
> 		<!--<link  />-->
> 		
> 	</head>
> 	<body>
> 		<a href="text.html">超链接一</a>
> 		<a>超链接二</a>
> 		<a>超链接三</a>
> 		
> 	</body>
> </html>
> ```

#### 12.框架标签【了解】

> <frameset></frameset>:划分规则【父标签】
>
> ​	rows:按照行进行划分
>
> ​	cols:按照列进行划分
>
> ​	<frame>：具体显示的页面【子标签】
>
> 注意：不能写在body中，不能写在body外面，使用了框架标签之后，则需要将body去掉
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
> 	
> 	<!--列分：cols-->
> 	<!--<frameset cols="30%,50%,20%">
> 		<frame src="1.超链接标签的使用一.html"/>
> 		<frame src="4.音视频标签的使用.html"/>
> 		<frame src="6.表单标签的使用二【了解】.html"/>
> 	</frameset>-->
> 	
> 	<!--行分-->
> 	<!--<frameset rows="30%,50%,20%">
> 		<frame src="1.超链接标签的使用一.html"/>
> 		<frame src="4.音视频标签的使用.html"/>
> 		<frame src="6.表单标签的使用二【了解】.html"/>
> 	</frameset>-->
> 	
> 	<!--混合分-->
> 	<frameset rows="20%,*">
> 		<frame src="1.超链接标签的使用一.html" />
> 		<frameset cols="40%,*">
> 			<frame src="4.音视频标签的使用.html"/>
> 			<frame src="6.表单标签的使用二【了解】.html"/>
> 		</frameset>
> 	</frameset>
> </html>
> ```

### 