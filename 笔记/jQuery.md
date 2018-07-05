### 一、jQuery

#### 1.简介

> 是一个封装了javascript的轻量级的库
>
> jQuery包含的功能：
>
> ```
> html元素的获取
> 
> html元素的操作
> 
> css操作
> 
> html事件函数
> 
> 特效和动画
> 
> DOM
> 
> AJAX【网络请求】
> ```
>
> 使用jq的好处：
>
> ```
> a.将之前js代码简化
> 
> b.不需要关心兼容性问题
> 
> c.提供了大量的函数
> ```
>
> 使用jq的思想：
>
> ```
> a.模拟css中的选择器工作
> 
> b.独特的语法
> 
> c.一套筛选元素的方式
> ```
>
> 注意：工作的核心就是选择器

#### 2.jQuery使用选择器的优势

> a.代码更加简单
>
> ```
> 将js中常用的函数做了封装，并且简化
> 
> 举例：document.getElementById("box")
> 
> 	    $("#box")
> ```
>
> b.支持所有的css【css1-css3】
>
> ```
> 支持css中所有的选择器，并且jQuery中有自己独特的选择器
> ```

#### 3.安装

> http://jquery.com
>
> 方式一：直接引入jQuery对应的js文件
>
> <script src="js的相对路径"></script>
>
> 方式二:引用网络资源

#### 4.第一个jQuery程序

> 代码演示：

> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入js文件-->
> 		<script src="js/jquery-3.3.1.js" type="text/javascript"></script>
> 	</head>
> 	<body>
> 		<script>
> 			//1.js中的页面加载函数
> 			//特点：window.onload只能被使用一次,如果出现多次，则后出现的会覆盖掉前面出现的
> 			/*window.onload = function(){
> 				alert("hello");
> 			}
> 			
> 			window.onload = function(){
> 				alert("hello~~~~~~");
> 			}*/
> 			
> 			//2.jQuery中的页面加载函数
> 			//特点：$(document).ready可以出现多次，并且按照出现的顺序依次执行
> 			$(document).ready(function(){
> 				alert("hello");
> 			})
> 			$(document).ready(function(){
> 				alert("hello!~~~~~~~");
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 5.jQuery基本语法

> 通过美元符定义
>
> 基本语法格式：$(选择器).methodName()
>
> 其中，选择器：css中的选择器，jq的独特的选择器
>
> $(选择器)：匹配到的元素的对象
>
> 对象.函数（）
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
> 			#box{
> 				width: 100px;
> 				height: 100px;
> 				background-color: red;
> 			}
> 		</style>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div id="box"></div>
> 		<script>
> 			$(document).ready(function(){
> 				//1.js获取div对象
> //				var jsDiv = document.getElementById("box");
> //				jsDiv.innerHTML = "hello";
> 
> 
> 				//2.jq获取div对象
> 				var $jqDiv = $("#box");
> 				$jqDiv.html("hello");
> 				
> 				//合并
> 				//$("#box").html("hello");
> 				
> 				
> 				//注意：两者之间的函数的调用不能混用
> 				
> 				//jq和js的对象之间可以进行相互转化
> 				//jq----->js
> 				var jsDiv1 = $jqDiv[0];
> 				var jsDiv2 = $jqDiv.get(0);
> 				
> 				//js----->jq
> 				var $jqDiv2 = $(jsDiv1);
> 				
> 			});
> 		</script>
> 	</body>
> </html>
> ```

### 二、jQuery选择器

#### 1.基本选择器

##### 1.1ID选择器

> 语法：$("#id")
>
> 作用：通过id匹配元素

##### 1.2元素选择器

> 语法：$("标签名称")
>
> 作用：通过标签名称匹配元素

##### 1.3类选择器

> 语法：$(".class的值")
>
> 作用：通过class属性的值匹配元素

##### 1.4复合选择器

> 语法：$(“selector1,selector2......selectorn”)
>
> 作用：通过不同的选择器匹配元素

##### 1.5通配符选择器

> 语法：$("*")
>
> 作用：可以匹配所有的标签

> 代码演示：

> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入js文件-->
> 		<script src="js/jquery-3.3.1.js" type="text/javascript"></script>
> 	</head>
> 	<body>
> 		<div id="box1" class="cls"></div>
> 		<div id="box2" class="cls"></div>
> 		<p></p>
> 		<script>
> 			$(document).ready(function(){
> 				//id选择器
> 				var $div = $("#box1");
> 				
> 				
> 				//元素选择器
> 				//getElementByTagName
> 				var $div1 = $("div");
> 				
> 				//类选择器
> 				//getElementByClassName
> 				var $div2 = $(".cls");
> 				
> 				
> 				//复合选择器
> 				var $jqObj = $(".cls,p");
> 				
> 				
> 				//通配符选择器
> 				var $jqObj1 = $("*");
> 				
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 2.层次选择器

##### 2.1ancetor descendant先辈后辈选择器

> 语法：$("ancetor descendant")
>
> 作用：类似于css中包含选择器

##### 2.2parent>child父子选择器

> 语法：$("parent>child")
>
> 作用：类似于css中包含选择器

##### 2.3prev+next兄弟选择器

> 语法：$("prev+next")
>
> 作用：用于匹配紧跟在prev后面的一个元素

##### 2.4prev~sibling选择器

> 语法：$("prev~sibling")
>
> 作用：用于匹配紧跟在prev后面的所有元素

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入js文件-->
> 		<script src="js/jquery-3.3.1.js" type="text/javascript"></script>
> 	</head>
> 	<body>
> 		
> 		<div id="box1">
> 			<p></p>
> 			<div>
> 				<p id="p"></p>
> 			</div>
> 		</div>
> 		
> 		<ul id="ul">
> 			<li id="li"></li>
> 			<li></li>
> 		</ul>
> 		
> 		
> 		<div id="box2" class="cls"></div>
> 		<div class="cls1"></div>
> 		<div class="cls2"></div>
> 		<div class="cls3"></div>
> 		<div class="cls4"></div>
> 		
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//先辈后辈选择器
> 				//注意：匹配到的是后辈标签
> 				var $jqObj1 = $("#box1 #p");
> 				
> 				
> 				//父子选择器
> 				//注意：匹配到的是子标签
> 				var $jqObj2 = $("ul>li");
> 				var $jqObj3 = $("#ul>#li");
> 				
> 				
> 				//兄弟选择器
> 				//prev + next
> 				var $jqObj4 = $("#box2+div");//cls1
> 				
> 				//prev + sibling
> 				var $jqObj5 = $("#box2~div");//cls1~cls4
> 			})
> 		</script>
> 	</body>
> </html>
> ```
>
> 

#### 3.过滤选择器

> 特点： 冒号

##### 3.1简单过滤器

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		
> 		<p class="pp">aaaaaa</p>
> 		<p class="pp">bbbb</p>
> 		<p class="pp">ccccc</p>
> 		<p class="pp">ddddd</p>
> 		<p class="pp">eeeeee</p>
> 		
> 		<p class="p1">eeeeee</p>
> 		
> 		<h1>标题</h1>
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//类似于css中的伪类选择器
> 				//：first  只匹配第一个符合条件的标签对象
> 				$(".pp:first").html("AAAAA");
> 				
> 				//:last  只匹配最后符合条件的标签对象
> 				$(".pp:last").html("last");
> 				
> 				//:even :  匹配所有编号为偶数的元素,从0开始
> 				$(".pp:even").html("even");
> 				
> 				//:odd:    匹配所有编号为奇数的元素
> 				$(".pp:odd").html("odd");
> 				
> 				//:eq(index)   匹配指定编号的元素
> 				$(".pp:eq(1)").html("11111");
> 				
> 				//:gt(index)   匹配所有大于给定编号的元素
> 				//注意：不包含指定编号
> 				$(".pp:gt(1)").html("gggggtttttt");
> 				
> 				//：lt(index)    匹配所有小于给定编号的元素
> 				//注意：不包含指定编号
> 				$(".pp:lt(1)").html("llllltttttt");
> 				
> 				//:header   匹配h1~h6的元素
> 				$(":header").html("fhsurghj");
> 				
> 				
> 				//:not(selector):  去除所有能够匹配上的元素【否定】
> 				$("p:not(.pp)").html("notnotnot");
> 				
> 				//：animated    匹配所有正在执行动画的元素
> 				$(":animated").html("fhsurghj");
> 				
> 			})
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 3.2内容过滤器

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入js文件-->
> 		<script src="js/jquery-3.3.1.js" type="text/javascript"></script>
> 	</head>
> 	<body>
> 		<p class="pp">aaaaaaa</p>
> 		<p class="pp">bbbbbhtml</p>
> 		
> 		<p class="pp">
> 			<font>aaa</font>
> 		</p>
> 		
> 		
> 		<table>
> 			<tr>
> 				<td>
> 					<p id="id">good</p>
> 				</td>
> 				<td>
> 					<p>study</p>
> 				</td>
> 			</tr>
> 		</table>
> 		
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//:contains(xx)  匹配包含指定文本的内容所对应的元素【掌握】
> 				//注意：指定的子字符串在原字符串中存在【连续存在】
> 				var $jqObj1 = $("p:contains('bbht')").html("html");
> 				
> 				
> 				//:empty    匹配文本为空的元素
> 				var $jqObj2 = $(".pp:empty").html("empy");
> 				
> 				
> 				//:has(selector)    匹配含有指定选择器的标签
> 				var $jqObj3 = $("td:has(#id)");
> 				
> 				
> 				//:parent    匹配含有子标签的元素
> 				var $jqObj3 = $("p:parent");
> 					
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### 3.3可见性过滤器

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入js文件-->
> 		<script src="js/jquery-3.3.1.js" type="text/javascript"></script>
> 	</head>
> 	<body>
> 		
> 		<input type="text" value="aaa" />
> 		
> 		<!--隐藏元素-->
> 		<!--方式一-->
> 		<input type="hidden" value="bbbbb" />
> 		
> 		<!--方式二-->
> 		<input type="text" style="display: none;" value="cccc"/>
> 		
> 		
> 		
> 		<script>
> 			$(document).ready(function(){
> 				
> 					//元素的可见状态分为两类：可见，不可见【display:none】
> 					//:visible
> 					//：hidden
> 					
> 					var $jqObj1 = $("input:visible").val("hello");
> 					
> 					
> 					//注意：获取input的值，如果有多个，则只能获取第一个匹配到的元素的值
> 					var $jqObj2 = $("input:hidden");
> 					console.log($jqObj2.val());
> 					
> 					
> 					//过滤选择器可以在原来的选择器的基础上再继续过滤
> 					var $jqObj3 = $("input:hidden:last");
> 			})
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 3.4表单对象的属性过滤器

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入js文件-->
> 		<script src="js/jquery-3.3.1.js" type="text/javascript"></script>
> 	</head>
> 	<body>
> 		
> 		<form>
> 			复选框1：<input type="checkbox" checked="checked" value="check1" />
> 			复选框2：<input type="checkbox" checked="checked" value="check2" />
> 			复选框3：<input type="checkbox" value="check3" />
> 			<br />
> 			
> 			<input type="button"  value="不可用按钮" disabled/>
> 			<br />
> 			
> 			<select>
> 				<option value="option1">1</option>
> 				<option value="option2">2</option>
> 				<option value="option3">3</option>
> 			</select>
> 			
> 		</form>
> 		
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//；checked   匹配所有被选中的元素【掌握】
> 				var $jqObj1 = $("input:checked:eq(0)");
> 				
> 				
> 				//:disabled  匹配所有不可用的元素
> 				var $jqObj2 = $("input:disabled");
> 				
> 				//:enabled: 匹配所有可用的元素		
> 			})
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 3.5表单子元素过滤器

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入js文件-->
> 		<script src="js/jquery-3.3.1.js" type="text/javascript"></script>
> 	</head>
> 	<body>
> 		
> 		<ul>
> 			<li>选项1</li>
> 			<li>选项2</li>
> 			<li>选项3</li>
> 			<li>选项4</li>
> 			<li>选项5</li>
> 		</ul>
> 		
> 		<ul>
> 			<li>选项1111</li>
> 		</ul>
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//结构选择器
> 				//:first-child	匹配第一个子元素【掌握】
> 				var $jqObj1 = $("ul li:first-child");
> 				
> 				//:last-child	匹配最后一个子元素
> 				
> 				//：only-child   如果某个元素是它的父元素的唯一的子元素，则会被匹配
> 				var $jqObj2 = $("ul li:only-child");
> 				
> 				//:nth-child(index)  匹配父元素下的第几个子元素【掌握】
> 				var $jqObj3 = $("ul li:nth-child(0)");
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 4.属性选择器

> 选择器[属性]
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
> 			div{
> 				width: 100px;
> 				height: 100px;
> 				background-color: red;
> 			}
> 		</style>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<!--通过元素的属性作为过滤条件-->
> 		<div name="div1">第一个div</div>
> 		<div name="div2">第2个div</div>
> 		<div name="div3">第3个div</div>
> 		<div>第4个div</div>
> 		<div name="box">第5个div</div>
> 		<div name="div3">第6个div</div>
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//[attr]   匹配所有给定属性的元素
> 				$("div[name]").css("background-color","green");
> 				
> 				//[attr=value]   匹配所有给定属性的元素
> 				$("div[name='div3']").css("background-color","blue");
> 				
> 				//[attr!=value]   否定
> 				$("div[name!='div3']").css("background-color","yellow");
> 				
> 				//[attr*=value]  至少一次
> 				$("div[name*='div3']").css("background-color","cyan");
> 				
> 				//[attr^=value]   匹配以value开头的元素
> 				$("div[name^='div']").css("background-color","gray");
> 				
> 				
> 				//[attr$=value]   匹配以value结尾的元素
> 				$("div[name$='div']").css("background-color","gray");
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 5.表单选择器

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<form>
> 			<input type="text"  name="normal"/>
> 			<input type="password" />
> 			<input type="file" />
> 			<input type="checkbox" />
> 			<input type="radio" />
> 			<input type="image" />
> 			
> 			<input type="button" />
> 			<input type="submit" />
> 			<input type="reset" />
> 		</form>
> 		<script>
> 			$(document).ready(function(){
> 				//匹配多选框
> 				var $jqObj = $(":checkbox");
> 				
> 				//:radio
> 				//:image   匹配图片
> 				//:password  密码
> 				
> 				//需求：匹配第一个input的选择器
> 				//$("input:first")
> 				//$("input[name]")
> 				//$(":text")
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 6.选择器中的注意事项

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div id="box#test"></div>
> 		
> 		<div class="name">
> 			<div style="display: none;">小科</div>
> 			<div style="display: none;">小王</div>
> 			<div style="display: none;">小张</div>
> 			<div style="display: none;" class="name">小李</div>		
> 		</div>
> 		
> 		<div style="display: none;" class="name">小liu</div>
> 		<div style="display: block;" class="name">小yang</div>		
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//1.特殊符号
> 				//如果选择器中出现#，.  ,(,[等特殊符号的时候，需要对这些特殊符号进行转义
> 					//转义：\\
> 				var $jqObj = $("#box\\#test");
> 				
> 				//2.含有空格
> 				//先辈后辈选择器【包含选择器】
>  				var $jqObj1 = $(".name :hidden");
> 				
> 				//过滤选择器
> 				var $jqObj2 = $(".name:hidden")
> 				
> 			})
> 		</script>
> 	</body>
> </html>
> ```

### 三、jQuery操作元素

#### 1.操作文本内容

> text()
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		
> 		<div>
> 			<p>fhahfjahfja</p>
> 		</div>
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * text():用于获取某个指定元素的文本值
> 				 * 
> 				 * text(value):用于给指定的元素设置值
> 				 */
> 				//获取
> 				//var text = $("div").text();
> 				//document.write(text);
> 				
> 				//设置
> 				//注意：只是用来设置纯文本，并不能把html标签识别
> 				//$("div").text("hello");
> 				$("div").text("<span>文本内容</span>");
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 2.操作html内容

> html()
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div>
> 			<p>fhahfjahfja</p>
> 		</div>
> 		
> 		<div>
> 			<p>hello</p>
> 		</div>
> 		
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * html():用于获取第一个匹配到的元素的html内容      第一个
> 				 *   
> 				 * html(value):设置所有匹配到的元素的html内容      所有
> 				 * 
> 				 */
> 				//获取
> 				//console.log($("div").html());
> 				
> 				//设置
> 				//设置纯文本
> 				//$("div").html("aaaaaa");
> 				//设置html标签
> 				$("div").html("<span>文本内容</span>");
> 				
> 				
> 				/*
> 				 * text和html函数之间的区别
> 				 * 区别：text只能设置纯文本。html可以设置html标签
> 				 * 相同点：不传参表示获取，传参表示设置
> 				 * 
> 				 * 
> 				 * <div>
> 						<p>hello</p>
> 				   </div>
> 				 * div的文本内容：hello
> 				 * div的html内容：<p>hello</p>
> 				 */	
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 3.操作元素值

> val()
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<input type="text" value="123" />
> 		<input type="text" value="456" />
> 		<script>
> 			$(document).ready(function(){
> 				/*主要和value属性有关
> 				 * 
> 				 * val():获取第一个匹配到的元素的元素值
> 				 * val(value):设置所有匹配到的元素的值
> 				 * 
> 				 */
> 				
> 				//获取
> 				//console.log($("input").val());
> 				
> 				//设置
> 				$("input").val("hello");
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 4.操作元素的css样式

> css()
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
> 			.box{
> 				background-color: red;
> 			}
> 			
> 			.change1{
> 				
> 			}
> 			
> 			.change2{
> 				
> 			}
> 			
> 			
> 		</style>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div class="box"></div>
> 		<script>
> 			$(document).ready(function(){
> 				
> 				//第一部分：修改css的类
> 				/*
> 				 * addClass():为所有匹配到的元素添加css类
> 				 * removeClass()：为所有匹配到的元素删除css类
> 				 * toggleClass()：如果css类存在，则删除，如果不存在，则添加
> 				 */
> 				
> 				
> 				//作用：虽然class的属性值并不是changge1,但是.change1类选择器中的样式可以作用于div
> 				//使用场景：在代码执行的过程中，可以动态给某个标签设置样式
> 				$("div").addClass("change1");
> 				$("div").removeClass("change1");
> 				
> 				
> 				
> 				//第二部分：修改css属性
> 				/*
> 				 * css(name):返回第一个匹配到的元素的指定属性的值
> 				 * css(name,value):为所有匹配到的元素设置指定的属性值
> 				 */
> 				
> 				//设置多个属性值s
> 				//$("div").css({"width":"100px","height":"100px"});
> 				
> 				//设置单个属性值
> 				$("div").css("background-color","red");
> 				
> 				
> 				//获取
> 				$("div").css("background-color");
> 			})
> 		</script>
> 	</body>
> </html>
> ```

### 四、jQuery操作DOM【掌握】

#### 1.创建节点

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div></div>
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * 创建元素节点
> 				 * 创建文本节点
> 				 * 创建属性节点
> 				 * 
> 				 * 
> 				 * append()  添加子节点
> 				 */
> 				
> 				//创建元素节点
> 				var $jqObj = $("<p></p>");
> 				$("div").append($jqObj);
> 				
> 				
> 				//创建文本节点
> 				var $jqObj = $("<p>hello</p>");
> 				$("div").append($jqObj);
> 				
> 				
> 				//创建属性节点
> 				var $jqObj = $("<p name='pp'>hello</p>");
> 				$("div").append($jqObj);
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 2.插入节点

##### 2.1在元素内部插入

##### 2.2在元素外部插入

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		
> 		
> 		<div>
> 			<!--<p></p>-->
> 		</div>
> 		
> 		<!--<div></div>-->
> 		
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * 1.在元素内部插入节点：添加子节点
> 				 * append(content):为所有匹配到的元素添加内容【后置内容】
> 				 * appendTo(content):
> 				 * 
> 				 * prepend(content):为所有匹配到的元素添加内容【前置内容】
> 				 * prependTo(content)
> 				 * 
> 				 */
> 				var $jqObj = $("<p>today</p>");
> 				$("div").append($jqObj);
> 				
> 				
> 				/*
> 				 * 2.在元素外部插入节点：添加兄弟节点
> 				 * after()
> 				 * insertAfter()    在每个匹配到的元素的后面插入一个指定节点
> 				 * 
> 				 * before()
> 				 * insertBefore()   在每个匹配到的元素的前面插入一个指定节点
> 				 */ 
> 				
> 				$("div").after($("<div>today</div>"));
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 3.删除节点

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div>
> 			<p>hjfahfa</p>
> 			<p>kkkkkkkk</p>
> 		</div>
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * remove()：删除匹配到的所有的元素，将绑定的事件全部删除
> 				 * detach()：删除匹配到的所有的元素，将绑定的事件保留下来
> 				 * 
> 				 * empty():清空
> 				 */
> 				
> 				//返回值：被删除掉的节点对象
> 				var $jqObj = $("div p":eq(1)).remove();
> 				$("div").append($jqObj);
> 				
> 				//注意：并不是删除节点，而是将节点清空，可以清空该节点的子节点
> 				$("div p:eq(1)").empty();
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 4.复制节点

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div>
> 			<p></p>
> 			<p></p>
> 		</div>
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * clone() ；复制的是匹配到的元素
> 				 * 
> 				 * clone(boolean):
> 				 * 	true:复制匹配到的元素以及绑定的事件
> 				 * 	false:只复制匹配到的元素
> 				 */
> 				
> 				$("div p:eq(0)").clone(true);
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 5.替换节点

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div id="div1"></div>
> 		<div id="div2"></div>
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * replaceAll()
> 				 * 
> 				 * replaceWith()
> 				 * 
> 					替换能够匹配到的节点
> 				 */
> 				
> 				$("#div1").replaceWith("<div>替换字符串</div>");
> 				
> 				$("<div>替换字符串</div>").replaceAll("#div2");
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 6.包裹节点

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<p>
> 			<span></span>
> 		</p>
> 		
> 		
> 		<span>hello</span>
> 		<span>html</span>
> 		<span>aaaaa</span>
> 		<span>hhhhhh</span>
> 		
> 		<span>
> 			<b></b>
> 		</span>
> 		
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * wrap()  将匹配到的元素使用指定的元素包裹起来
> 				 * unwrap() 
> 				 * 
> 				 * wrapAll()
> 				 * 
> 				 * wrapInner()
> 				 */
> 				
> 				//wrap:把匹配到的每一个元素用p标签包裹起来
> 				$("span").wrap("<p></p>");
> 				
> 				//unwrap:将span标签外面包裹的标签去除
> 				$("span").unwrap();
> 				
> 				//wrapInner() ------>append   添加子标签
> 				$("span").wrapInner("<b></b>");
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 7.遍历节点

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<img src="" />
> 		<img src="" />
> 		<img src="" />
> 		<img src="" />
> 		<img src="" />
> 		
> 		<script>
> 			$(document).ready(function(){
> 				//each(callback):callback是一个函数，该函数可以接收一个形参index，这个index表示遍历的节点的序号
> 				
> 				//jQuery
> 				$("img").each(function(index){
> 					//获取到的每一个img标签对象
> 					var $jqObj = $(this);
> 					$jqObj.attr("title","image" + index);
> 				})
> 				
> 				
> 				//js
> 				var imgList = document.getElementsByTagName("img");
> 				for(var i = 0;i < imgList.length;i++) {
> 					var img = imgList[i];
> 					img.setAttribute("title","image" + index);
> 				}
> 				
> 			})
> 		</script>
> 	</body>
> </html>
> ```

### 五、动画

#### 1.隐藏/显示

#### 2.切换可见状态

#### 3.淡入/淡出

#### 4.滑动

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<style>
> 			#box{
> 				width: 100px;
> 				height: 200px;
> 				background-color: cyan;
> 			}
> 		</style>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div id="box"></div>
> 		
> 		<button id="btn1">隐藏</button>
> 		<button id="btn2">显示</button>
> 		
> 		<button id="btn3">切换可见状态</button>
> 		
> 		
> 		<button id="btn4">淡入</button>
> 		<button id="btn5">淡出</button>
> 		
> 		
> 		<button id="btn6">向上滑动</button>
> 		<button id="btn7">向下滑动</button>
> 		
> 		<button id="btn8">切换滑动状态</button>
> 		
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * hide(time，callback):
> 				 * show()
> 				 * 说明：time表示动画持续的时间，callback是一个回调函数，动画执行结束之后需要进行的操作
> 				 * 
> 				 * 
> 				 * toggle():实现元素的可见状态的切换，如果元素是可见的，则让他不可见；
> 				 * 
> 				 * fadeIn()
> 				 * fadeOut()
> 				 * 
> 				 * slideDown():从上往下滑动，
> 				 * slideUp()：从下往下滑动
> 				 * slideToggle()
> 				 */
> 				
> 				
> 				//给按钮绑定一个事件，作用等同于js中的事件的属性
> 				//参数：事件类型   回调函数
> 				$("#btn1").bind("click",function(){
> 					//$("#box").hide();
> 					//time:单位为毫秒，默认事件为600ms，normal【400ms】，slow【600ms】,fast【200ms】
> 					$("#box").hide(1000,function(){
> 						console.log("隐藏动画结束");
> 					});
> 				})
> 				$("#btn2").bind("click",function(){
> 					
> 					$("#box").show(1000,function(){
> 						console.log("显示动画结束");
> 					});
> 				})
> 				//hide是从下往上消失，show从上往下依次显示 
> 				
> 				
> 				$("#btn3").bind("click",function(){
> 					
> 					$("#box").toggle(1000,function(){
> 						console.log("切换元素的可见状态");
> 					});
> 				})
> 				
> 				
> 				$("#btn4").bind("click",function(){
> 					
> 					$("#box").fadeIn(2000,function(){
> 						console.log("淡入");
> 					});
> 				})
> 				$("#btn5").bind("click",function(){
> 					
> 					$("#box").fadeOut(2000,function(){
> 						console.log("淡出");
> 					});
> 				})
> 				
> 				//滑动
> 				$("#btn6").bind("click",function(){
> 					
> 					$("#box").slideUp(2000,function(){
> 						console.log("向上滑动");
> 					});
> 				})
> 				$("#btn7").bind("click",function(){
> 					
> 					$("#box").slideDown(2000,function(){
> 						console.log("向下滑动");
> 					});
> 				})
> 				
> 				
> 				$("#btn8").bind("click",function(){
> 					
> 					$("#box").slideToggle(2000,function(){
> 						console.log("切换滑动状态");
> 					});
> 				}}	
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 5.自定义动画

> animate({parmas},time,callback)
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
> 			#box{
> 				width: 200px;
> 				height: 200px;
> 				background-color: orange;
> 			}
> 		</style>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div id="box"></div>
> 		<button>指定动画</button>
> 		<script>
> 			$(document).ready(function(){
> 				$("button").bind("click",function(){
> 					//1.设置单个css属性
> 					/*$("#box").animate({height:'800px'},2000,function(){
> 						
> 					})*/
> 					
> 					//2.设置多个css属性
> 					$("#box").animate({
> 						height:'800px',
> 						width:'500px',
> 						opacity:'0.5'
> 					},2000,function(){
> 					
> 					})
> 					
> 				})
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```
>
> 应用：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<style>
> 			*{
> 				padding: 0px;
> 				margin: 0px;
> 			}
> 			
> 			body{
> 				background-image: url(img/bg.jpg);
> 			}
> 			
> 			#container{
> 				width: 100%;
> 				height: 100%;
> 			}
> 			
> 			img{
> 				width: 40px;
> 				height: 40px;
> 				position:absolute;
> 			}
> 			
> 		</style>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div id="container">
> 			
> 		</div>
> 		<script>
> 			$(document).ready(function(){
> 				
> 				//需求：每隔2秒，在页面上出现一个萤火虫，实现动画效果
> 				//间歇性定时器
> 				setInterval(function(){
> 					
> 					//创建一个img节点
> 					var $fireworm  = $("<img src='img/萤火虫.jpg'/>");
> 					
> 					//将创建好的节点添加到div节点下面【在元素内部插入节点】
> 					$("#container").append($fireworm);
> 					
> 					//获取随机数，定位img的位置
> 					var wLeft = Math.ceil(Math.random() * 1000) + "px";
> 					var wTop = Math.ceil(Math.random() * 600) + "px";
> 					
> 					//设置img每次出现的位置
> 					$fireworm.css({
> 						left:wLeft,
> 						top:wTop
> 					})
> 					
> 					//每次让img限定在屏幕范围内【边界检测】
> 					//获取屏幕的宽高
> 					var sWidth = $("#container").width();
> 					var sHeight = $("#container").height();
> 					
> 					
> 					//实现萤火虫的动画
> 					function fireWormFly(){
> 						console.log(sWidth);
> 						var fLeft = Math.ceil(Math.random() * sWidth) + "px";
> 						var fTop = Math.ceil(Math.random() * sHeight) + "px";
> 						
> 						$fireworm.animate({
> 							left:fLeft,
> 							top:fTop
> 						},3000,function(){
> 							fireWormFly();
> 							
> 							
> 						});
> 					}
> 					//调用函数
> 					fireWormFly();
> 						
> 				},2000);
> 			})
> 		</script>
> 	</body>
> </html>
> ```

### 上堂回顾

> 1.选择器
>
> ​	基本选择器：css类比【标签名称，id，类，通配符，组合】
>
> ​	层次选择器：父子标签，先辈后辈标签【父子标签】，兄弟标签【+ 、  ~】
>
> ​	属性选择器：基本选择器[指定的属性]、基本选择器[指定的属性 = 值]
>
> 2.操作元素
>
> ​	操作文本和html内容：text()   html()
>
> ​	操作元素值：val()
>
> ​	操作css样式：
>
> ​		类：addClass("类名")    removeClass()
>
> ​		属性：css({})   css("属性名"，“属性值”)
>
> 3.操作DOM
>
> ​	创建节点，插入节点，删除节点等
>
> ​	重点：节点树【根节点，元素节点，属性节点，文本节点】
>
> ​	节点对象
>
> 4.动画
>
> ​	参数：time/speed    回调函数
>
> ​	hide()、show()
>
> ​	toggle()
>
> ​	fadeIn() , fadeOut()
>
> ​	slideDown()     slideUp()   slideToggle()
>
> ​	自定义动画：animate({},speed,callback)

### 六、jQuery中的事件

#### 1.页面加载事件

> $(docuement).ready(function(){})
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<script>
> 			//事件模块中最重要的一个函数，很大程度上提高了web的响应速度
> 			/*$(document).ready(function(){
> 			})*/
> 			
> 			//简写方式一
> 			/*$().ready(function(){
> 			})*/
> 			
> 			//简写方式二
> 			$(function(){
> 					
> 			})
> 			
> 			/*
> 			 * 【面试题：$(document).ready(function()和window.onload之间的区别】
> 			 * 1.$(document).ready(function()在一个页面中可以出现多次，执行的顺序按照出现的先后顺序执行的
> 			 *  window.onload只能出现一次，执行的时候只执行最后出现的
> 			 * 2.当一个网页完全下载到浏览器的时候【文本，包括关联的文件：图片，视频，音频等】，就会相应window.onload
> 			 * 	$(document).ready方法只有当元素加载完成之后即可响应【网页解析元素的速度比加载文件的速度快的多】
> 			 */
> 			
> 			//类似于window.onload的作用，jQuery中的写法
> 			$(window).load(function(){
> 				
> 			});
> 			
> 			//完全等价于
> 			window.onload = function(){}
> 			
> 		</script>
> 	</body>
> </html>
> ```

#### 2.jQuery中的事件处理

##### 2.1事件绑定

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<button id="btn">添加</button>
> 		<div>
> 			<p>1111</p>
> 			<p>2222</p>
> 			<p>333</p>
> 			<p>444</p>
> 		</div>
> 		
> 		<script>
> 			$(function(){
> 				//事件绑定：bind()    delegate()  事件类型（）  on()  live()   
> 				
> 				//1.bind()
> 				/*bind(type,[data],fn)
> 				 * type:事件类型
> 				 * data:可选参数，结合事件对象使用，event.data
> 				 * fn：绑定的事件处理函数
> 				 */
> 				/*$("#btn").bind("click",function(){
> 					
> 					$("div").append("<p>新的p标签</p>");
> 				})*/
> 				
> 				//需求：点击p标签的时候给div添加子标签p
> 				/*$("div p").bind("click",function(){
> 					
> 					$("div").append("<p>新的p标签</p>");
> 				})*/
> 				
> 				/*
> 				 * 问题
> 				 * 1.这里包含了隐式的迭代，如果匹配到的元素特别多的时候，元素的事件绑定可能会重复很多次，
> 				 *   对于大量元素而言，影响了性能
> 				 * 2.对于尚未存在的元素，无法自动绑定事件，必须进行手动的二次绑定
> 				 */
> 				
> 				
> 				//2.delegate()
> 				/*
> 				 * 代理委托设计模式
> 				 * 代理：帮忙解决问题的对象
> 				 * 委托：让其他对象解决问题的对象
> 				 * 
> 				 * 事件委托，也被称为事件代理，利用事件的冒泡模式【从内到外】给父元素添加响应事件，从而使得所有的子元素都可以有响应事件
> 				 * 
> 				 * 优点：
> 				 * 	1.减少DOM操作，提高交互效率
> 				 *  2.新添加的元素同样可以有响应事件
> 				 * 
> 				 * 适用场景：如果所有的子元素都要求实现相同的事件效果，这个时候可以考虑将事件绑定到父元素上
> 				 *          父元素充当的是代理，子元素充当的是委托
> 				 * 
> 				 * 适用事件【冒泡类型的事件】：click mousedown mouseup keydown keyup mousemove
> 				 * 
> 				 * 用法：代理对象.delegate("委托对象"，type，事件的响应函数)
> 				 */
> 				/*$("div").delegate("p","click",function(){
> 					$("div").append("<p>新的p标签</p>");
> 				})*/
> 				
> 				/*
> 				 * 问题：
> 				 * 绑定是变得容易了，但是调用的时候也可能会出现问题，如果事件元素在DOM树中处于比较深的位置
> 				 * 这样事件一层一层冒泡上来查找相关的父元素，同时影响到了性能
> 				 */
> 				
> 				//3.on（）
> 				//on是bind函数和delegate函数的升级版
> 				//格式：对象.on(type,"事件委托"，事件的响应函数)
> 				/*$("div").on("click","p",function(){
> 					$("div").append("<p>新的p标签</p>");
> 				})*/
> 				
> 				
> 				//4.事件名称(事件的响应函数)
> 				$("#btn").dblclick(function(){
> 					console.log("hello");
> 				})
> 				
> 				
> 				//5.live()
> 				
> 				/*
> 				 * 总结；
> 				 * 1.选择匹配的元素比较多的时候，不推荐使用bind
> 				 * 2.用id选择器，使用bind最方便
> 				 * 3.需要给元素动态绑定事件，推荐使用delegate或者on
> 				 * 4.使用delegate的时候，注意DOM树不要太深
> 				 * 5.on最安全最优化的
> 				 */	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### 2.2事件解绑

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<button id="btn">添加</button>
> 		<div>
> 			<p>1111</p>
> 			<p>2222</p>
> 			<p>333</p>
> 			<p>444</p>
> 		</div>
> 		<script>
> 			$(document).ready(function(){
> 				//1.unbind(type)
> 				/*$("#btn").bind("click",function(){
> 					
> 					$("div").append("<p>新的p标签</p>");
> 				})*/
> 				//注意：一个标签对象上可能会绑定多种事件，所以解绑的时候必须要指定解绑的时间类型
> 				$("#btn").unbind("click");
> 				
> 				//2.undelegate()
> 				/*$("div").delegate("p","click",function(){
> 					$("div").append("<p>新的p标签</p>");
> 				})*/
> 				//注意：undelegate解绑的时候需要指明委托和事件类型
> 				$("div").undelegate("p","click");
> 				
> 				
> 				//3.off()
> 				/*$("div").on("click","p",function(){
> 					$("div").append("<p>新的p标签</p>");
> 				})*/
> 				$("div").off("click","p");
> 	
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### 2.3绑定一次性事件

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<button id="btn">按钮</button>
> 		<script>
> 			$(document).ready(function(){
> 				/*
> 				 * 作用：当点击按钮的时候只触发一次事件，当第二次点击的时候将不起作用
> 				 * one(type,[data],fn)
> 				 * 
> 				 */
> 				$("#btn").one("click",function(){
> 					console.log("hello");
> 				})
> 				
> 				//注意：使用bind，delegate以及on也可以实现一次性事件，只不过是先绑定，然后再合适的时机解绑
> 				
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### 2.4模仿悬停事件

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--<style>
> 			div:hover{
> 				
> 			}
> 		</style>-->
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div style="width: 100px; height: 100px; background-color: red;"></div>
> 		<script>
> 			$(document).ready(function(){
> 				
> 				/*
> 				 * 通过hover函数模仿鼠标的悬浮事件
> 				 * 注意：鼠标移动到元素上方的时候需要做什么样的操作
> 				 * 		鼠标移出的时候需要做什么操作
> 				 * 
> 				 * hover(over,out)
> 				 * over:用于指定当鼠标移动到元素上方的时候需要触发的 函数
> 				 * out:用于指定鼠标移出元素的时候需要触发发的函数
> 				 * 
> 				 * 工作原理：当鼠标移动到元素上方的时候，则触发over函数，移出的时候，触发的out函数
> 				 */
> 				
> 				$("div").hover(function(){
> 					
> 					//当鼠标移动到元素上方的时候需要设置的内容【css样式】
> 					console.log("over");
> 					
> 					$("div").html("hello");
> 					
> 				},function(){
> 					//当鼠标移出元素上方的时候需要设置的内容【css样式】
> 					console.log("out");
> 					
> 					$("div").css("background-color","cyan");
> 				});
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### 2.5事件对象

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="utf-8" />
> 		<title></title>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<button>按钮</button>
> 		<script>
> 			$(document).ready(function(){
> 				$("button").bind("click",function(event){
> 					console.log(event);
> 					
> 					//获取事件的类型
> 					console.log(event.type);
> 					
> 					//获取触发事件的元素
> 					console.log(event.target);
> 					
> 					//获取和事件相关联的元素
> 					console.log(event.relatedTarget);
> 					
> 					//获取光标相对于页面的x坐标和y坐标
> 					console.log(event.pageX,event.pageY);	
> 				})
> 			})
> 		</script>
> 	</body>
> </html>
> ```

#### 3.Swiper

> 代码演示：
>
> html