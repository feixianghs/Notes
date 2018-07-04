### 一、上堂回顾

> 1.事件
>
> ​	页面加载事件
>
> ​	事件绑定：bind,事件类型，delegate【思想】，on
>
> ​	事件解绑：unbind,undelegate,off
>
> ​	绑定一次性事件：one()
>
> ​	模仿鼠标悬浮事件：hover(over,out)
>
> ​	事件对象：event

### 二、AJAX

#### 1.简介

##### 1.1什么是AJAX

> AJAX：Asynchronous  Javascript   And XML,异步的js的xml
>
> AJAX并不是一门新的编程语言，而是用来创建动态网页的一门技术
>
> 作用：使用js语言与服务器进行异步交互
>
> 同步交互：客户端发出一个请求之后，需要等待服务端响应结束后，才能发出第二次请求
>
> 异步交互：客户端发出一个请求之后，无需等待服务端的响应，就可以发出第二次请求

##### 1.2优缺点

> 优点
>
> a.向服务端发送异步请求
>
> b.无需刷新整个页面【局部刷新】
>
> c.工作效率提高
>
> 缺点：
>
> a.并不是所有的场景都能使用AJAX，很多情况下还是需要使用同步交互
>
> b.虽然提高了用户体验，但是无形中向服务器发送请求的次数增多，服务器的压力也随着增大
>
> c.还需要处理浏览器兼容问题

##### 1.3使用场景

> a.关键字搜索
>
> ![关键字搜索](C:\Users\Administrator\Desktop\SZ-Python1805\web-Day11\笔记\关键字搜索.png)
>
> b.表单注册
>
> ![表单注册](C:\Users\Administrator\Desktop\SZ-Python1805\web-Day11\笔记\表单注册.png)

##### 1.4js实现局部刷新

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
> 		<h1>注册页面</h1>
> 		<form action="#" method="get" id="form1">
> 			用户名：<input type="text" name="username" id="username" />
> 			<span id="userspan"></span>
> 			<br />
> 			<input type="submit" value="提交" />
> 			
> 		</form>
> 		<script>
> 			window.onload = function(){
> 				//1.获取表单标签对象
> 				var form = document.getElementById("form1");
> 				//为了校验数据，当数据不合法的时候阻止表单提交
> 				form.onsubmit = function(){
> 					//2.获取input标签的value值
> 					//form.username.value
> 					var input = document.getElementById("username");
> 					var val = input.value;
> 					
> 					if(!val){
> 						//3.用户名不合法，阻止表单提交
> 						var span = document.getElementById("userspan");
> 						span.innerHTML = "用户名不能为空！";
> 						
> 						return false;
> 					}
> 					
> 					return true;
> 				}
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 1.5技术

> 四步操作【针对的是原生的AJAX】
>
> a.创建核心对象
>
> b.使用核心对象打开和服务器之间的连接
>
> c.发送请求
>
> d.注册监听，监听服务端的响应
>
> 涉及到的类或者方法
>
> a.XMLHTTPRequest类
>
> b.open(请求方式，请求的地址，是否异步)
>
> c.send(请求体)
>
> d.onreadystatechange,指定监听事件，当状态发生改变的时候会被调用
>
> e.readyState:获取状态，取值范围为1~4，4表示服务器响应结束
>
> f.status:服务器的状态码，只有服务器响应的时候才会有值，200表示响应成功
>
> g.responseText:获取服务端的响应数据

#### 2.使用

##### 2.1原生的AJAX

##### a.表单的get请求

> 代码演示：
>
> php文件
>
> ```php
> <?php
> header('content-type:text/html;charset="utf-8"');
> error_reporting(0);
> //$_REQUEST
> $username = $_POST['username'];
> $age = $_POST['age'];
> $password = $_POST["password"];
> 
> echo "你的名字：{$username}，年龄：{$age}，密码：{$password}";
> ?>
> ```
>
> html文件
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
> 		<!--
> 			get请求
> 			http://10.36.131.122/formGet.php?username=grfg&age=65&password=feg
> 			
> 			表单的提交分为get和post，默认的提交方式为get
> 			
> 			特点：
> 			将字段和数值使用=连接，如果有多个键值对的时候，使用&连接，最终将所有拼接好的数据拼接到url的后面
> 		-->
> 		
> 		<form action="http://10.36.131.122/formGet.php" method="get">
> 			<!--注意：name属性的取值必须和服务端的字段保持完全的一致-->
> 			<input type="text" name="username" />
> 			<input type="text" name="age" />
> 			<input type="password" name="password" />
> 			<input type="submit" value="提交" />
> 		</form>
> 	</body>
> </html>
> ```

##### b.表单的post请求

> 代码演示：
>
> php文件
>
> ```php
> <?php
> header('content-type:text/html;charset="utf-8"');
> error_reporting(0);
> //$_REQUEST
> $username = $_POST['username'];
> $age = $_POST['age'];
> $password = $_POST["password"];
> 
> echo "你的名字：{$username}，年龄：{$age}，密码：{$password}";
> ?>
> ```
>
> html文件
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<!--
> 			注意：通过浏览器内部进行数据的传输
> 			设置编码格式：enctype="application/x-www-form-urlencoded"
> 			
> 			
> 			优点:安全。比较适合传输较大的数据
> 			缺点：麻烦，效率较低
> 		-->
> 		<form action="http://10.36.131.122/formPost.php" method="post">
> 			<!--注意：name属性的取值必须和服务端的字段保持完全的一致-->
> 			<input type="text" name="username" />
> 			<input type="text" name="age" />
> 			<input type="password" name="password" />
> 			<input type="submit" value="提交" />
> 		</form>
> 	</body>
> </html>
> ```

##### c.AJAX的get请求

> 代码演示：
>
> php文件
>
> ```php
> <?php
> header('content-type:text/html;charset="utf-8"');
> header('Access-Control-Allow-Origin:*');  
> error_reporting(0);
> //就是系统或应用程序出错时弹出的 错误报告，编程人员根据这个报告的内容可以判断是哪一段程序代码出问题了。
> $username = $_GET['username'];
> $age = $_GET['age'];
> $password = $_GET["password"];
> 
> /*获取?后面对应健的值*/
> 
> echo "你的名字：{$username}，年龄：{$age}，密码：{$password}";?>
> ```
>
> html文件
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<button id="get">获取</button>
> 		<script>
> 			window.onload = function(){
> 				var btn = document.getElementById("get");
> 				btn.onclick = function(){
> 					//请求数据
> 					//1.创建请求对象
> 					var xhr = null;   //兼容问题
> 					//try-except    try-catch
> 					try{
> 						xhr = new XMLHttpRequest();
> 					}catch(e){
> 						//IE
> 						xhr = new ActiveXObject("Microsoft.XMLHTTP");
> 					}
> 					
> 					//2.与服务端建立连接
> 					//注意：get请求的特点是将参数拼接在url中
> 					//参数：请求方式，请求的服务器的地址，是否需要异步
> 					//http://10.36.131.122/formGet.php?username=grfg&age=65&password=feg
> 					//encodeURI("")
> 					var name = encodeURI("杨阳");
> 					xhr.open("get","http://10.36.131.122/ajaxGet.php?username=" + name + "&age=18&password=abc123",true);
> 				
> 					//3.发送请求
> 					xhr.send();
> 					
> 					//4.建立监听，监听服务端的响应
> 					xhr.onreadystatechange = function(){
> 						/*readyState：当前对象的状态
> 						 * 	1,2,3,4，最终是4表示请求完成
> 						 * 
> 						 *status:状态码
> 						 * 	200：成功
> 						 * 	404：数据不存在
> 						 * 	400：加载错误
> 						 * 	500：数据库错误
> 						 */
> 						if(xhr.readyState == 4 && xhr.status == 200){
> 							alert("数据请求成功" + xhr.responseText);
> 						}else{
> 							//请求失败
> 						}
> 					}
> 				}
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### d.AJAX的post请求

> 代码演示：
>
> php文件：
>
> ```php
> <?php
> header('content-type:text/html;charset="utf-8"');
> header('Access-Control-Allow-Origin:*');  
> error_reporting(0);
> //$_REQUEST
> $username = $_POST['username'];
> $age = $_POST['age'];
> $password = $_POST["password"];
> 
> echo "你的名字：{$username}，年龄：{$age}，密码：{$password}";
> ?>
> ```
>
> html文件
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<button id="get">获取</button>
> 		<script>
> 			window.onload = function(){
> 				var btn = document.getElementById("get");
> 				btn.onclick = function(){
> 					//请求数据
> 					//1.创建请求对象
> 					var xhr = null;   //兼容问题
> 					//try-except    try-catch
> 					try{
> 						xhr = new XMLHttpRequest();
> 					}catch(e){
> 						//IE
> 						xhr = new ActiveXObject("Microsoft.XMLHTTP");
> 					}
> 					
> 					//2.与服务端建立连接
> 					//注意：get请求的特点是将参数拼接在url中
> 					//参数：请求方式，请求的服务器的地址，是否需要异步
> 					//http://10.36.131.122/formGet.php?username=grfg&age=65&password=feg
> 					//encodeURI("")
> 					var name = encodeURI("杨阳");
> 					xhr.open("post","http://10.36.131.122/ajaxPost.php",true);
> 					
> 					//2.5指定数据的编码格式:设置请求的请求头,固定写法
> 					xhr.setRequestHeader("content-type","application/x-www-form-urlencoded");
> 					
> 				
> 					//3.发送请求【发送请求体】
> 					var message  = "username=" + name + "&age=18&password=abc123";
> 					xhr.send(message);
> 					
> 					//4.建立监听，监听服务端的响应
> 					xhr.onreadystatechange = function(){
> 						/*readyState：当前对象的状态
> 						 * 	1,2,3,4，最终是4表示请求完成
> 						 * 
> 						 *status:状态码
> 						 * 	200：成功
> 						 * 	404：数据不存在
> 						 * 	400：加载错误
> 						 * 	500：数据库错误
> 						 */
> 						if(xhr.readyState == 4 && xhr.status == 200){
> 							alert("数据请求成功" + xhr.responseText);
> 						}else{
> 							//请求失败
> 						}
> 					}
> 				}
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 2.2jQuery中的AJAX

##### a.load方法

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<div id="box"></div>
> 		<button>请求</button>
> 		<script>
> 			$(function(){
> 				/*
> 				 * load(url,[data,callback])
> 				 * url:请求html页面的地址【网络资源或者本地资源的相对路径】
> 				 * data:可选参数，发送到服务器的数据【以key：value】
> 				 * callback:可选参数，回调函数，当加载html页面成功之后需要调用的函数
> 				 * 
> 				 */
> 				
> 				//1.载入html文档
> 				/*$("button").click(function(){
> 					$("#box").load("index.html");
> 				})*/
> 				
> 				//2.
> 				//注意：可以加载任意的html文件
> 				$("button").click(function(){
> 					$("#box").load("index.html",function(responseText,status,request){
> 						//当加载html页面成功之后执行的操作
> 						
> 					});
> 				})
> 				
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### b.get和post方法

> $.get()
>
> $.post()
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<form>
> 			<input type="text" id="username" />
> 			<textarea id="content"></textarea>
> 			<input type="button" id="button" value="提交" />
> 		</form>
> 		<script>
> 			$(function(){
> 				/*
> 				 * $.get(url[,data,callback,type])
> 				 * 
> 				 */
> 				/*$("#button").bind("click",function(){
> 					//使用jQuery中的ajax发起请求【get】
> 					$.get("http://10.36.131.122/formGet.php",
> 					{username:$("#username").val(),content:$("#content").val()},function(data){
> 						//获取到了服务端的响应
> 						//data.username   data.content
> 					})
> 				})*/
> 				
> 				/*
> 				 * $.post(url[,data,callback,type])
> 				 */
> 				
> 				$("#button").bind("click",function(){
> 					//使用jQuery中的ajax发起请求【get】
> 					$.post("http://10.36.131.122/formGet.php",
> 					{username:$("#username").val(),content:$("#content").val()},function(data){
> 						//获取到了服务端的响应
> 						//data.username   data.content
> 					})
> 				})
> 				 
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### c.getScript方法

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<!--<script src="js/alert.js"></script>-->
> 		<input type="button" id="btn" value="点击" />
> 		<div class="box">hello</div>
> 		<div class="box">html</div>
> 		<script>
> 			$(function(){
> 				/*
> 				 * $.getScript(url,callback)
> 				 * 加载js文件，可以动态的加载外部的js文件，js文件会自动被执行，提高了工作效率
> 				 */
> 				
> 				$.getScript("js/alert.js",function(){
> 					$("#btn").click(function(){
> 						$(".box").css("background-color","cyan");
> 					})
> 				})
> 			})
> 		</script>
> 	</body>
> </html>
> ```

##### d.ajax方法

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<script type="text/javascript" src="js/jquery-3.3.1.js"></script>
> 	</head>
> 	<body>
> 		<form>
> 			<input type="text" id="username" />
> 			<textarea id="content"></textarea>
> 			<input type="button" id="button" value="提交" />
> 		</form>
> 		<script>
> 			$(function(){
> 				/*
> 				 * $.ajax():$.get和$.post函数的综合体
> 				 * $.ajax(type,url,data,callback)
> 				 */
> 				$("#button").click(function(){
> 					$.ajax({
> 						type:"get",
> 						url:"",
> 						data:{username:$("#username").val(),content:$("#content").val()},
> 						async:true
> 					});
> 				}) 
> 			})
> 		</script>
> 	</body>
> </html>
> ```

