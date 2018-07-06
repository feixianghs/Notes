### 一、Javascript简介

#### 1.概念

> Netscape【网景公司】与Sun公司开发的一门脚本语言
>
> 是基于对象和事件驱动的脚本语言，应用在客户端【浏览器】，简称js
>
> ​	基于对象：提供好了很多对象，可以直接使用
>
> ​	事件驱动：js实现动态效果【事件】
>
> js的作用:操作html和css	

#### 2.特点

> 交互性：实现信息的动态交互
>
> 安全性：不可以直接访问磁盘上的文件
>
> 跨平台性：只要是可以解析js的浏览器都可以执行，与平台无关

#### 3.Javascript和Java

> 【雷锋和雷峰塔：JavaScript和Java没有任何关系，属于两门编程语言】
>
> a.开发公司
>
> ​	Java是sun公司开发的，现在是oracle公司
>
> ​	JS是Netscape【网景公司】公司开发的
>
> b.对象
>
> ​	Java是面向对象的【new】
>
> ​	JS是基于对象的
>
> c.数据类型
>
> ​	Java是强类型语言【每种变量都有确定的数据类型】例如：int i = “10”;
>
> ​	JS是弱类型语言【变量的类型由值决定】例如：var i = 10; var j = “10”;		
>
> d.执行过程
>
> ​	Java需要现编译成字节码文件，然后再执行
>
> ​	JS只需解析就可以执行

#### 4.js的组成

> a.ECMAScript
>
> ​	ECMA:欧洲计算机协会
>
> ​	指定js的基本语法：变量，运算符，语句，函数。。。。
>
> b.BOM
>
> ​	Broswer Object Model:浏览器对象模型
>
> c.DOM
>
> ​	Document Object Model,文档对象模型

### 二、使用

#### 1.js和html的结合方式

##### 1.1内部方式

> ```javascript
> <script type="text/javascript">js代码</script>
> ```
>
> 写法：可以写在body中，也可以写在head中
>
> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--结合方式一：内部方式，可以写在head或者body中-->
> 		<script type="text/javascript">
> 			alert("hello world")
> 		</script>
> 	</head>
> 	<body>
> 		<script type="text/javascript">
> 			alert("hello world~~~~~~~1")
> 		</script>
> 		<script type="text/javascript">
> 			alert("hello world~~~~~~~2")
> 		</script>
> 		<script type="text/javascript">
> 			alert("hello world~~~~~~~3")
> 		</script>
> 		
> 		<!--script标签可以出现多次，先执行head中的，再执行body中，body中的script按照从上往下的顺序依次执行-->
> 	</body>
> </html>
> ```

##### 1.2引用外部js文件

> ```javascript
> <script type="text/javascript" src="外部js文件的相对路径"></script>
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
> 		<script type="text/javascript" src="js/text.js">
> 			//单行注释[ctrl + /]：当你已经引入了外部的js文件时，在script标签中再书写js代码将不起作用，毫无意义
> 			/*
> 			 * 多行注释[ctrl + shift + /]
> 			 */
> //			alert("内部~~~~~~")
> 		</script>
> 		<script>
> 			alert("内部~~~~~~")
> 		</script>
> 	</body>
> </html>
> ```

### 三、ECMAScript的基本语法

#### 1.定义变量

> Python：num = 10
>
> 语法：
>
> var 变量名 = 初始值
>
> var num = 10;
>
> 注意：每条语句后面最好能添加一个分号
>
> 代码演示:
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<script>
> 			//1.先声明，后赋值
> 			var num;
> 			num = 10;
> 			
> 			//2.可以在声明的同时进行赋值
> 			var num1 = 20;
> 			
> 			//3.同时定义多个变量
> 			//var只需要书写一次，不同变量之间使用逗号隔开
> 			var name = "zhangsan",age = 18;
> 			
> 			//4.js是弱类型语言，容错性较高，在赋值的时候才能确定具体的数据类型【Python完全类型】
> 			var b;    //不确定数据类型
> 			b = 10;  //int
> 			b = "hello";   //字符串
> 			
> 		</script>
> 	</body>
> </html>
> ```

#### 2.命名规范

> **a.由数字，字母，下划线和美元符[$]**
>
> **b.不能以数字和空格开头，并且不能包含空格**
>
> **c.不能使用关键字**
>
> **d.区分大小写**
>
> **e.遵循驼峰命名法**

#### 3.js的数据类型

> Python：数字型【整型，浮点型】，字符串，布尔型，列表，元组，字典，集合，空值None
>
> js：
>
> ​	一般数据类型：Number，Boolean，String，Object，Array数组，函数Function，RegExp正则
>
> ​	特殊数据类型：
>
> ​		Null：表示一个变量指向空，使用**typeof   操作符检测null返回object**
>
> ​		Undefined：定义一个变量，但是这个变量没有被赋予初始值
>
> ​		NaN：Not a  Number,不是一个数字

##### 3.1一般数据类型

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
> 		<script>
> 			var str = "10";
> //			alert(str)
> 			
> 			var num = 10;
> //			alert(num)
> 			
> 			var boo = true;
> 			
> 			//使用typeof函数或者操作符判断一个变量的数据类型
> 			//alert(typeof(num));
> 			alert(typeof num);
> 				
> 		</script>
> 	</body>
> </html>
> ```

##### 3.2特殊数据类型

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
> 		<script>
> 			//1.Null
> 			var c = null;   //c = None
> 			document.write(typeof c)   //object
> 			
> 			document.write("<br />");
> 			
> 			//2.Undefined
> 			var b;
> 			document.write(b);
> 			
> 			document.write("<br />");
> 			
> 			//注意：undefined其实派生自null，所以二者表示的值是相同的
> 			document.write(undefined == null);  //true
> 			
> 			//注意：此处c1和b1的数据类型是不同的
> 			var c1;
> 			var b1 = null;
> 			document.write(typeof c1 == typeof b1);
> 			document.write("<br />");
> 			
> 			
> 			//3.NaN
> 			var a = 10 / 0;
> 			document.write(a);  //Infinity
> 			var a1 = 0 / 0;
> 			document.write(a1);  //NaN
> 			
> 			document.write("<br />");
> 			
> 			//isNaN():判断某个变量是不是NaN，是Number返回false   不是Number返回true
> 			document.write(isNaN("hello"));  //true
> 			document.write(isNaN("10"));  //false
> 			document.write(isNaN(10));  //false
> 			
> 			//注意：当接收道一个数据的时候，两个作用：作用一：判断是不是一个number，作用二：会尝试将数据转换为number
> 			
> 			//注意：在js中，boolean可以转换为number，true和false分别代表是1和0
> 			document.write(isNaN(true));
> 			document.write(isNaN(false));
> 				
> 		</script>
> 	</body>
> </html>
> ```

#### 4.运算符

##### 4.1算术运算符

> Python + - * / // %  **
>
> js:+ - * /  %     ++    --:自增自减运算符
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
> 		<script>
> 			//++和--跟在变量的前面或者后面使用，都表示将变量本身加1或者减1
> 			
> 			//++
> 			var n = 2;
> 			var r = ++n;
> 			var n1 = 2;
> 			var r1 = n1++;
> 			document.write(n);
> 			document.write(r);
> 			document.write(n1);
> 			document.write(r1);
> 			//3332
> 			
> 			//注意：当++出现在变量的前面：变量本身先增1，然后整体参与表达式的运算中
> 			//	       当++出现在变量的后面：先将变量参与到表达式的运算中，然后才自增1
> 			
> 			
> 			var num1 = 3;
> 			var result1 = ++num1 + 2;
> 			document.write(num1);   //4
> 			document.write(result1); //6
> 			
> 			var num2 = 3;
> 			var result2 = num2++ + 2;
> 			document.write(num2);  //4
> 			document.write(result2);//5
> 			
> 			
> 			//--
> 			var num3 = 3;
> 			var result3 = --num3 + 2;
> 			document.write(num3);   //2
> 			document.write(result3); //4
> 			
> 			var num4 = 3;
> 			var result4 = num4-- + 2;
> 			document.write(num4);  //2
> 			document.write(result4);//5
> 			
> 			//注意：++和--跟在变量的前面或者后面，可以单独使用
> 			//++num   =====> num = num + 1
> 			var a = 10;
> 			a++;   //++a;
> 			document.write(a);
> 			document.write("<br />");
> 			
> 			
> 			//+  ：拼接运算符
> 			//在js中，字符串和任意数据类型使用+，得到的结果都为字符串
> 			document.write("10" + 1);
> 			document.write("<br />");
> 			document.write("hello" + 22);
> 			document.write("<br />");
> 			document.write("10" + "22");
> 			document.write("<br />");
> 			document.write("abc" + true);
> 			document.write("<br />");
> 			document.write("10" + null);
> 			document.write("<br />");
> 			document.write("10" + undefined);
> 				
> 		</script>
> 	</body>
> </html>
> ```

##### 4.2关系运算符

> 注意：
>
> a.应用在if语句或者循环中
>
> b.结果为布尔值
>
> c.如果字符串比较，比较的是字符编码值【字典】
>
> **d.number和字符串进行比较，则会尝试将其中的字符串转换为number，然后才进行比较**

##### 4.3逻辑运算符

> Python：and   or   not
>
> **js:&&   ||   !**
>
> **注意：使用规律和Python中完全相同，同样会出现短路原则**

##### 4.4赋值运算符

> =
>
> += -=等
>
> num += 10    ======》 num = num + 10

##### 4.5三目运算符【三元运算符】

> 格式：关系运算符 ？值1：值2
>
> 说明：
>
> ​	a.值1和值2可以是常量，变量，表达式
>
> ​	b.工作原理：如果关系表达式成立，则三目运算符返回值1，否则返回值2
>
> ​	c.作用：实现二选一的操作
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
> 		<script>
> 			//判断一个数是否是偶数
> 			/*
> 			 * num = 10
> 			 * if num % 2 == 0:
> 			 * 	  #偶数
> 			 * else:
> 			 * 	  #奇数
> 			 */
> 			
> 			//常量
> 			var num = 10;
> //			var result = num % 2 == 0 ? "偶数" : "奇数";
> 			var result = num % 2 == 0 ? true : false;
> 			document.write(result);
> 			
> 			
> 			//变量
> 			var r1 = true;
> 			var r2 = false;
> 			
> 			var result1 = num % 2 == 0 ? r1 : r2;
> 			
> 			
> 			//表达式
> 			var result2 = num % 2 == 0 ? (3 != 5) : (3 == 5);
> 			
> 			//注意：三目运算符本质上是一个运算符，执行完成之后肯定会得到一个结果，使用一个变量将这个结果接出来
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 4.6特殊用法

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
> 		<script>
> 			//1.只有一个除法运算：/
> 			
> 			//2.js中的字符串可以进行相加或者相减的运算
> 			//+：拼接
> 			//-：实际的数学运算【前提条件：字符串可以转换为number】
> 			//特殊情况：如果字符串无法转换为number，-：得到的结果为NaN
> 			var str = "456";
> 			document.write(str + 1);  //4561
> 			document.write("<hr />");
> 			document.write(str - 1);
> 			document.write("<hr />");
> 			document.write("abc" - 1);
> 			
> 			//3.布尔型的变量也可以和number类型的变量进行运算
> 			var flag1 = true;
> 			document.write(flag1 + 1);
> 			
> 			var flag2 = false;
> 			document.write(flag2 + 1);
> 			
> 			
> 			//4.=  ==  ===
> 			//=:赋值运算符
> 			//==：关系运算符
> 			//===：关系运算符
> 			var aa = "5";
> 			if(aa == 5){
> 				document.write("相等");
> 			}else{
> 				document.write("不相等");
> 			}
> 			//相等
> 			
> 			var bb = "5";
> 			if(bb === 5){
> 				document.write("相等");
> 			}else{
> 				document.write("不相等");
> 			}
> 			//不相等
> 			
> 			//总结：==只比较的是值，===比较的是类型和值	
> 		</script>
> 	</body>
> </html>
> ```

#### 5.语句

> Python语句：
>
> ​	分支：if,if-else  ,if-elif-else
>
> ​	循环：while,for-in
>
> js:
>
> ```js
> 	分支：if,if-else,if-else if -else,switch
> 	循环：简单for，for-in,while,do-while
> ```
>
> 5.1if语句
>

> 语法：
>
> 单分支：
>
> if(条件表达式){
>
> }
>
> 双分支：
>
> if(条件表达式){
>
> } else{
>
> }
>
> 多分支：
>
> if(条件表达式1){
>
> } else if(条件表达式2){
>
> }else if(条件表达式3){
>
> }
>
> 。。。。
>
> else{
>
> }
>
> 注意：如果if语句中代码只有一行的时候，可以省略掉{}
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
> 		<script>
> 			//单分支
> 			//要么执行，要么不执行
> 			var num1 = 100;
> 			if(num1 < 100){
> 				document.write("成立");
> 			}
> 			
> 			//双分支
> 			//实现二选一的操作，类似于三目运算符的使用，二者之间可以进行相互转换
> 			if(num1 % 2 == 0){
> 				document.write("偶数");
> 			}else{
> 				document.write("奇数");
> 			}
> 			
> 			//多分支
> 			//不管有多少个分支，每次都只会执行其中的一个分支，则表示整个多分支结束
> 			var n = 3;
> 			if(n > 1){
> 				document.write("aa");
> 			}else if(n > 2){
> 				document.write("bb");
> 			}else if(n > 3){
> 				document.write("cc");
> 			}else{
> 				document.write("dd");
> 			}
> 			
> 			//三者之间的区别
> 			if(n > 1){
> 				document.write("aa");
> 			}
> 			
> 			if(n > 2){
> 				document.write("bb");
> 			}else{
> 				document.write("cc");
> 			}
> 			
> 			if(n > 3){
> 				document.write("ee");
> 			}else if(n > 4){
> 				document.write("dd");
> 			}else{
> 				document.write("ff");
> 			}
> 			
> 			//嵌套语句
> 			if(n > 1){
> 				if(n > 2){
> 					document.write("ok");
> 				}
> 			}
> 			if(n > 1 && n > 2){
> 				document.write("ok");
> 			}
> 			
> 			//书写一个永远成立的条件
> 			if(true){
> 				
> 			}
> 			if(1){
> 				
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 5.2switch语句

> **作用：类似于if语句中的多分支，实现多选一的操作**
>
> 语法：
>
> switch(变量){
>
> ​	case 常量1：{
>
> ​		执行语句1；
>
> ​		break；
>
> ​	}
>
> ​	case 常量2：{
>
> ​		执行语句2；
>
> ​		break；
>
> ​	}
>
> ​	。。。。
>
> ​	default：{
>
> ​		执行语句n；
>
> ​	}
>
> }
>
> 说明：
>
> 工作原理:根据变量的值去进行匹配，如果case分支后面的常量值能够匹配到，则执行对应的case分支，从上往下依次查找，如果所有的case分支都无法匹配，则执行default分支
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
> 		<script>
> 			//需求：有人加你好友，如果是女的，则欣然接受，如果是男的，则残忍拒绝，如果不明性别，则你不做任何处理
> 			//b:男   g:女
> 			
> 			var str = "h";
> 			
> 			switch(str){
> 				
> 				
> 				case "b":{
> 					document.write("残忍拒绝");
> 					break;
> 				}
> 				case "g":{
> 					document.write("欣然接受");
> 					break;
> 				}
> 				
> 				default:{
> 					document.write("不做处理");
> //					break;
> 				}
> 				
> 			}
> 			
> 			//1.break的作用：阻止向下穿透的作用【跳出整个switch语句】
> 			//2.永远都是先执行case分支，最后执行default分支【switch语句的执行顺序和其中的case以及default的书写顺序没有关系】
> 			//3.一般情况下，将default分支写在最后，如果将default写在case的前面或者中间，则需要在default语句中添加break
> 			//4.switch中的变量最好和case分支后的常量是同种数据类型，否则没有可比性
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 5.3while语句和do-while语句

> 语法：
>
> while语句：
>
> 初始化表达式；
>
> while(条件表达式){
>
> ​	循环体；
>
> ​	循环之后的操作表达式；
>
> }
>
> do-while语句
>
> 初始化表达式；
>
> do{
>
> ​	循环体；
>
> ​	循环之后的操作表达式；
>
> }while(条件表达式)；
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
> 		<script>
> 			//while
> 			var num1 = 0;
> 			while(num1 < 10){
> 				document.write(num1 + "<br />");
> 				num1++;
> 			}
> 			
> 			//do-while
> 			var num2 = 0;
> 			do{
> 				document.write(num2 + "<br />");
> 				num2++;
> 			}while(num2 < 10);
> 			
> 			
> 			//区分：
> 			var n1 = 3;
> 			while(n1 < 1){
> 				document.write("hello");
> 			}
> 			
> 			var n2 = 3;
> 			do{
> 				document.write("hello~~~~~");
> 			}while(n2 < 1);
> 			
> 			/*
> 			 * while：先判断条件是否成立，再去执行循环体
> 			 * do-while:先执行循环体，然后再去判断条件是否成立
> 			 * 结论：do-while不管条件成立与否，都至少会执行一次
> 			 * while使用频率更广
> 			 */
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 5.4for语句

> 语法：
>
> 简单for循环：
>
> for(初始化表达式；条件表达式；循环之后的操作表达式){
>
> ​	循环体；
>
> }
>
> for-in循环：
>
> for(变量 in 数组){
>
> ​	
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
> 	</head>
> 	<body>
> 		<script>
> 			var num1 = 0;
> 			while(num1 < 10){
> 				document.write(num1 + "<br />");
> 				num1++;
> 			}
> 			
> 			//简单for循环
> 			for(var n = 0;n < 10;n++){
> 				document.write(n + "<br />");
> 			}
> 			
> 			//for-in语句
> 			var arr = [43,54,6,56];
> 			for(num in arr){
> 				document.write(arr[num]);
> 			}
> 			
> 			document.write("<br />");
> 			
> 			//嵌套for语句
> 			for(var i = 1;i <= 9;i++){
> 				for(var j = 1;j <= i;j++) {
> 					document.write(j + "x" + i + "=" + i * j + "&nbsp;");
> 				}
> 				document.write("<br />");
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 5.5break和continue

> break:
>
> ​	在switch语句中表示跳出整个switch语句【分支语句】
>
> ​	在循环语句中跳出整个循环【就近原则】
>
> continue:
>
> ​	只能使用在循环语句中，使当前正在执行的循环结束，继续下一次的循环
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
> 		<script>
> 			//标签label
> 			//给不同的循环起别名，break根据循环的名字决定跳出的是具体是哪层循环
> 			loop1:
> 			for(var i = 0;i < 3;i++) {
> 				loop2:
> 				for(var j = 0; j < 5;j++) {
> 					document.write(i + "=" + j + "<br />");
> 					break loop2;
> 				}
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```

### 四、ECMAscript语法

#### 1.js中的函数

##### 1.1自定义函数

> 方式一：通过function关键字
>
> function 函数名（参数列表）{
>
> ​	函数体
>
> ​	return 返回值；
>
> }
>
> 方式二：匿名函数
>
> var 变量名= function(参数列表){
>
> ​	函数体
>
> ​	return 返回值；
>
> }
>
> 说明：
>
> ​	a.可以将匿名函数作为其他函数的参数使用
>
> ​	b.可以完成某些一次性的事件【DOM的事件】
>
> 方式三：使用js中的内置对象Function【动态函数，很少使用】
>
> Python：p = Person("")
>
> js:
>
> var 变量名 = new  Function（"参数列表"，“函数体和返回值”）
>
> js中的函数的调用
>
> 格式：函数名(实参)；
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
> 		<script>
> 			//1.function
> 			//定义一个无参无返回值的函数
> 			function text1(){
> 				document.write("hello");
> 			}
> 			//调用
> 			text1();
> 			
> 			//定义一个有参的函数，不需要返回值
> 			function add1(a,b){
> 				var sum = a + b;
> 			}
> 			add1(10,20);
> 			
> 			//定义一个有参有返回值的函数
> 			function add2(a,b){
> 				var sum = a + b;
> 				return sum;
> 			}
> 			r0 = add2(10,20);
> 			
> 			//2.匿名函数
> 			function text(func){
> 				func();
> 			}
> 			//匿名函数作为一个函数的参数使用
> 			text(function(){
> 				document.write("~~~~~");
> 			});
> 			
> 			
> 			var f = function(a,b){
> 				var sum = a + b;
> 			}
> 			f();
> 			
> 			//3.内置对象Function
> 			//参数：参数列表，函数体和返回自
> 			var r1 = new Function("x,y","var sum = x + y;return sum;");
> 			r0(10,20);
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 1.2全局函数

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
> 		<script>
> 			//1.eval():识别字符串中的js代码
> 			var str1 = "alert('hello')";
> 			//eval(str1);
> 			
> 			document.write("<hr />");
> 			
> 			//2.encodeURI():对字符编码
> 			var str2 = "中文测试abc123";
> 			var encode1 = encodeURI(str2);
> 			document.write(encode1);
> 			
> 			document.write("<hr />");
> 			
> 			//decodeURI():对字符解码
> 			var str3 = "%E4%B8%AD%E6%96%87%E6%B5%8B%E8%AF%95abc123";
> 			var decode1 = decodeURI(str3);
> 			document.write(decode1);
> 			
> 			document.write("<hr />");
> 			
> 			//3.isNaN():判断一个数据是不是不是一个数字
> 			
> 			//4.parseInt():类型转换【将传入的参数转换为整型int】
> 			var str4 = "123";
> 			document.write(str4 + 1);  //拼接
> 			
> 			document.write("<hr />");
> 			
> 			document.write(parseInt(str4) + 1); //实际数学运算
> 			
> 		</script>
> 	</body>
> </html>
> ```

#### 2.全局变量和局部变量

> 全局变量：在script标签中定义的变量，这个变量可以在当前html页面中的任何script标签中使用
>
> 局部变量：在函数内部定义的变量，只能在当前函数的内部使用
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
> 		<script>
> 			//全局变量
> 			var num1 = 10;
> 			
> 			//1.直接访问
> 			document.write(num1);
> 			
> 			//2.定义函数，在函数内部访问
> 			function check(){
> 				document.write(num1 + "~~~~~");
> 			}
> 			check();
> 			
> 			//局部变量
> 			function show(){
> 				var num2 = 20;
> 				document.write(num2);
> 			}
> 			
> 			
> 			//document.write(num2 + "%%%%%%");
> 			//校验数据：在浏览器中右键点击检查----》Console
> 			console.log(num2 + "%%%%%%");
> 			
> 		</script>
> 		<script>
> 			//3.在其他的script标签中访问
> 			document.write(num1 + "script");
> 			
> 			document.write(num2 + "script%%%%%%");
> 		</script>
> 	</body>
> </html>
> ```

#### 3.js中的对象

##### 3.1string对象

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
> 		<script>
> 			//一、字符串的创建方式
> 			var str1 = "abc";
> 			
> 			var str2 = new String("abc");
> 			
> 			var str3 = String("abc");
> 			
> 			//二、与字符串有关的函数
> 			//第一部分：和html有关的函数
> 			//1.字符串加粗
> 			var s1 = "hello";
> 			document.write(s1.bold());
> 			document.write(s1);
> 			
> 			document.write("<hr />");
> 			
> 			//2.设置字体大小和颜色
> 			//注意：fontsize的范围：1~7
> 			document.write(s1.fontcolor("red"));
> 			document.write(s1.fontsize(5));
> 			
> 			//3.将字符串显示为超链接
> 			var s2 = "点击";
> 			document.write(s2.link("http://www.baidu.com"));
> 			
> 			//4.设置上标和下标
> 			document.write(s1);
> 			document.write(s1.sub());
> 			document.write(s1.sup());
> 			
> 			//第二部分：和Python类似的函数
> 			//1.字符串拼接
> 			var string1 = "hello";
> 			var string2 = "html";
> 			document.write(string1.concat(string2));
> 			
> 			//2.获取指定位置上的字符
> 			//注意：如果字符位置不存在的，则返回一个空字符串
> 			var string3 = "abcdefg";
> 			document.write(string3.charAt(3));
> 			
> 			//3.获取某个子字符串在源字符串中第一次出现的位置
> 			//注意：如果子字符串在源字符串中不存在，则直接返回-1
> 			document.write(string3.indexOf("cde"));
> 			
> 			//4.切割字符串
> 			var string4 = "my name is zhangsan";
> 			var arr = string4.split(" ");
> 			document.write(arr.length);
> 			
> 			//5.字符串替换
> 			//注意：参数：old，new
> 			document.write(string4.replace("name","friends"));
> 				
> 		</script>
> 	</body>
> </html>
> ```

##### 3.2array对象

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
> 		<script>
> 			//一、数组的创建:array
> 			var arr1 = [1,2,3];
> 			
> 			//注意：初始化一个数组的容量
> 			var arr2 = new Array(3);
> 			
> 			var arr3 = new Array(1,2,3);
> 			
> 			
> 			//二、属性
> 			//获取数组的长度/数组中元素的个数
> 			var array1 = [23,5,65,65,6];
> 			document.write(array1.length);
> 			
> 			
> 			//三、函数
> 			//1.拼接
> 			document.write(arr1.concat(array1));
> 			
> 			//2.合并
> 			//作用：将数组转换为字符串
> 			var array2 = new Array(3);
> 			array2[0] = 10;
> 			array2[1] = 20;
> 			array2[2] = 30;
> 			document.write(array2.join("-"));
> 			
> 			//3.在数组的末尾添加元素
> 			//注意：返回值为数组中的元素的个数
> 			//注意：在js中，数组的使用和Python中的list是相似的，是可变数据
> 			document.write(array2.length);
> 			document.write(array2.push(40));
> 			document.write(array2.length);
> 			
> 			//4.从首部插入元素
> 			array2.unshift(50);
> 			
> 			//5.获取并删除最后一个元素
> 			document.write(array2.pop());
> 			
> 			//6.删除首元素
> 			array2.shift();
> 			
> 			
> 			//7.元素的反转
> 			document.write(array2.reverse());
> 			
> 			document.write("<hr  />");
> 			
> 			//8.数组的截取/获取子数组
> 			//注意：包头不包尾
> 			var array3 = [43,5,65,65,656,7,878,89];
> 			var array4 = array3.slice(3,6);
> 			document.write(array4);
> 				
> 		</script>
> 	</body>
> </html>
> ```

##### 3.3object对象

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
> 		<script>
> 			//1.创建一个object类型的变量
> 			//类似于Python中动态绑定属性
> 			var per = new Object();
> 			per.name = "zhangsan";
> 			per.age = 18;
> 			per.say = function(){
> 				document.write(per.name  + per.age);
> 			}
> 			per.say();
> 			
> 			//2.通过字面量的形式创建一个object类型的变量
> 			var p = {
> 				name:"jack",
> 				age:12,
> 				say:function(){
> 					document.write(this.name  + this.age);
> 				}
> 			}
> 			
> 			p.say();
> 			
> 			//访问方式：对象.
> 			document.write(p.name);
> 			//访问方式：类似于字典的用法
> 			document.write(p["name"]);
> 			
> 				
> 		</script>
> 	</body>
> </html>
> ```

##### 3.4math对象

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
> 		<script>
> 			//四舍五入
> 			document.write(Math.round(3.6));
> 			
> 			//向上取整
> 			document.write(Math.ceil(3.1));
> 			
> 			
> 			//向下取整
> 			document.write(Math.floor(3.1));
> 			
> 			//求最值：max  min
> 			
> 			//求绝对值
> 			document.write(Math.abs(-10));
> 			
> 			//求x的y次方
> 			document.write(Math.pow(2,3));
> 			
> 			//求x的平方根
> 			document.write(Math.sqrt(9));
> 			
> 			document.write("<br />");
> 			
> 			//求随机数
> 			document.write(Math.random());
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 3.5date对象

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
> 		<script>
> 			//一、date对象的创建
> 			//1.
> 			//注意：获取的是当前的日期，跟传入的字符串没有关系
> 			var date1 = Date("2016-9-18");
> 			document.write(date1);
> 			
> 			document.write("<br />");
> 			
> 			//2
> 			//默认获取到的是当前日期
> 			var date2 = new Date();
> 			document.write(date2);
> 			
> 			document.write("<br />");
> 			
> 			//获取到的是指定日期
> 			var date3 = new Date("2016-9-18");
> 			document.write(date3);
> 			
> 			document.write("<br />");
> 			
> 			//3
> 			var date4 = new Date(2016,9,18,0,0,0,100);
> 			document.write(date4);
> 			
> 			document.write("<br />");
> 			
> 			//4.通过时间戳获取指定的日期
> 			var date5 = new Date(42367462);
> 			document.write(date5);
> 			
> 			document.write("<br />");
> 			
> 			
> 			//二、函数
> 			var date = new Date();
> 			//第一部分：get
> 			document.write(date.getFullYear());
> 			document.write(date.getMonth());   //5
> 			document.write("<br />");
> 			document.write(date.getDay());  //一个星期中的第几天
> 			document.write("<br />");
> 			document.write(date.getDate());   //一个月中的第几天
> 			
> 			document.write("<br />");
> 			
> 			document.write(date.getTime());   //获取时间戳
> 			
> 			
> 			//第二部分：set
> 			date.setFullYear(2016);
> 	
> 			//0~11
> 			date.setMonth(12);
> 			document.write(date.getFullYear());  //2017
> 			
> 			
> 			date.setDate(32);
> 			
> 			document.write("<br />");
> 			
> 			//第三部分：
> 			
> 			document.write(date.toLocaleString());
> 			document.write("<br />");
> 			document.write(date.toLocaleTimeString());
> 			document.write("<br />");
> 			document.write(date.toLocaleDateString());
> 			
> 			document.write("<br />");
> 			
> 			//第四部分
> 			var date1 = new Date("2016-10-1 10:10:10");
> 			var date2 = new Date("2016-10-1 10:20:10");
> 			
> 			document.write(date2 - date1);  //数学减法
> 			
> 			document.write("<br />");
> 			
> 			document.write(date1 + date2); //拼接
> 			
> 		</script>
> 	</body>
> </html>
> ```

### 五、BOM

#### 1.简介

> 浏览器对象模型，是一个用来访问浏览器和计算机屏幕的对象的集合，可以通过全局变量window访问这个对象【通过window对象控制BOM】
>
> 注意：在js中定义的内容如果没有指明对象的话，则全部默认属于window的
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
> 		<script>
> 			var name = "hello";
> 			document.write(name);
> 			//注意：在js中定义的内容如果没有指明对象的话，则全部默认属于window的
> 			document.write(window.name);
> 		</script>
> 	</body>
> </html>
> ```

#### 2.window对象的使用

##### 2.1window中的BOM对象

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
> 				background-color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<button onclick="href()">跳转到绿色页面</button>
> 		<button onclick="refresh()">刷新当前页面</button>
> 		<button onclick="ass()">加载黄色页面</button>
> 		
> 		
> 		<button onclick="backPage()">上一页</button>
> 		<button onclick="forwardPage()">下一页</button>
> 		
> 		<button onclick="goPage()">go到黄色页面</button>
> 		
> 		
> 		<script>
> 			//了解
> 			//1.window.document:表示当前已经载入的文档对象【页面】，
> 			console.log(window.document);
> 			
> 			//2.window.frames；当前页面中所有框架的集合
> 			
> 			//3.window.navigator:反应浏览器以及功能信息的对象
> 			
> 			//4.window.screen：提供浏览器以外的环境信息
> 			
> 			
> 			//掌握
> 			//1.window.location
> 			/*
> 			 * href:控制浏览器地址栏中的内容
> 			 * reload():刷新页面/重载页面  reload(true):不带缓存的刷新
> 			 * assign():加载新的页面
> 			 * replace():加载新的页面【注意：不会再浏览器的历史记录中留下记录】
> 			 */
> 			console.log(window.location);
> 			
> 			function href(){
> 				window.location.href = "greenHtml.html";
> 			}
> 			
> 			//刷新
> 			function refresh(){
> 				window.location.reload();
> 			}
> 			
> 			function ass(){
> 				window.location.assign("yellowHtml.html");
> 				//window.location.replace("yellowHtml.html");
> 			}
> 			
> 			
> 			//注意：history对象的使用有一个前提：必须在浏览器中留下历史记录
> 			//2.window.history：历史记录
> 			/*
> 			 * length:获取历史记录的长度
> 			 * back()  ：后退
> 			 * forward()   ：前进
> 			 * go(num) ：num为负数的时候，则表示后退，num为正数的时候，表示前进
> 			 */
> 			function backPage(){
> 				window.history.back();
> 			}
> 			function forwardPage(){
> 				window.history.forward();
> 			}
> 			
> 			function goPage(){
> 				window.history.go(2);
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 2.2window中的函数

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
> 		<button onclick="openWindow()">打开</button>
> 		<button onclick="closeWindow()">关闭</button>
> 		<script>
> 			//打开的是指定页面
> 			function openWindow(){
> 				window.open("greenHtml.html","blank","width=200px,height=200px,left=0px,top=0px")
> 			}
> 			//关闭的是当前页面
> 			function closeWindow(){
> 				window.close();
> 			}
> 			
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 2.3window中的事件

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
> 				height: 3000px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<h1>我是个标题</h1>
> 		<button onclick="func()" style="position: fixed;right: 10px; bottom: 20px;">回到顶部</button>
> 		
> 		<script>
> 			//window对象的事件
> 			//onload：加载事件，当浏览器窗口加载的时候会自动触发事件【窗口加载完毕】
> 			/*window.onload = function(){
> 				document.write("hello");
> 			}*/
> 			
> 			//alert("~~~~~~");
> 			
> 			//onscroll：滚动事件，当浏览器窗口发生滚动的时候触发事件
> 			window.onscroll = function(){
> 				//获取滚动的高度
> 				//为了不同浏览器的兼容
> 				var scrollTop = document.documentElement.scrollTop  ||  document.body.scrollTop;
> 				console.log(scrollTop);
> 			}
> 			
> 			//回到顶部
> 			function func(){
> 				document.documentElement.scrollTop = 0;
> 				
> 				document.body.scrollTop = 0;
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```

#### 3.提示框

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
> 		<script>
> 			//1.警告框
> 			//特点：只有一个确定按钮
> 			//alert("hello");
> 			
> 			//2.提示框
> 			//特点：有取消按钮和确定按钮
> 			//返回的结果为布尔值
> 			/*var result = confirm("确定要删除吗？");
> 			if(result){
> 				//确定的操作
> 			} else{
> 				//取消的操作
> 			}*/
> 			
> 			//3.输入提示框
> 			//特点：输入框
> 			//参数：提示文字，默认值
> 			//返回值就是输入的数据
> 			var result1 = prompt("请输入一个数字",0);
> 			document.write(result1);
> 				
> 		</script>
> 	</body>
> </html>
> ```

#### 4.定时器

##### 4.1延时性定时器

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
> 		<button onclick="closeTimer()">关闭定时器</button>
> 		<script>
> 			//延时性定时器：只执行一次
> 			//参数：定时器触发的时候需要执行的函数，延时的时间长短【单位为毫秒】
> 			var timer = window.setTimeout(func,5000);
> 			
> 			function func(){
> 				console.log("hello");
> 			}
> 			
> 			//清除定时器
> 			function closeTimer(){
> 				window.clearTimeout(timer);
> 			}
> 			
> 			
> 			//注意：在编程语言中，没有实际的定时器的暂停和恢复，如果要暂停，一般的操作就是清除，如果要恢复，一般的操作就是重新创建一个定时器对象
> 		</script>
> 	</body>
> </html>
> ```

##### 4.2间歇性定时器

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
> 		<script>
> 			var timer = window.setInterval(func,2000);
> 			
> 			function func(){
> 				console.log("hello");
> 			}
> 			
> 			function closeInterval(){
> 				window.clearInterval(timer);
> 			}
> 		</script>
> 	</body>
> </html>
> ```

### 六、DOM

#### 1.简介

> 文档对象模型
>
> 可以使用js中dom里面提供的对象，使用这些对象的属性和方法，对html进行操作
>
> 工作原理：对html进行操作，首先将html文档封装成对象，对象：标签，文本，属性，封装成对象的目的是为了操作文档以及文档中的内容，因为对象包括属性和行为
>
> 明确一点：在加载html页面时，web浏览器会生成一个树形结构，用来表示页面内部结构，在DOM中被称为节点树

#### 2.常用方法和属性

> a.获取标签对象
>
> getElementById():根据id获取标签对象，获取到的只有一个对象
>
> getElementByTagName():根据标签名称获取标签对象，获取到的是多个标签对象
>
> getElementByName():根据name属性的值获取标签对象，获取到的是多个标签对象
>
> getElementByClassName():根据class属性的值获取标签对象，获取到的是多个标签对象
>
> b.节点的增删改查
>
> appendChild():追加子节点
>
> insertBefore():在指定子节点的前面插入节点
>
> removeChild():删除子节点
>
> replaceChild():替换子节点
>
> getAtttibute():获取指定的属性值
>
> c.创建节点
>
> createAttribute():创建属性节点
>
> createTextNode():创建文本节点
>
> createElement():创建元素节点
>
> d.属性
>
> innerHTML:获取或者设置文本值   ----->最常用的一个属性
>
> parentNode:获取父节点
>
> childNodes:获取子节点
>
> 
>
> nodeName:节点名称
>
> nodeType:节点类型
>
> nodeValue：获取节点的值

#### 3.方法和属性的使用

##### 3.1获取元素节点对象

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
> 		<input type="text" id="text1" value="aaaa" />
> 		<input type="text" id="text2" value="bbbb"  name="input1"/>
> 		<input type="text" id="text3" value="cccc"  name="input2"/>
> 		<input type="text" id="text4" value="dddd" name="input2"/>
> 		<input type="text" id="text5" value="eeee" class="inputClass"/>
> 		<input type="text" id="text6" value="ffff" class="inputClass"/>
> 		<script>
> 			//write；向浏览器页面中输出变量或者html代码
> 			var str  = "hello";
> 			document.write(str);
> 			//document.write("<input type='text' value='aaaa'/>");
> 			
> 			//docuement：文档对象，代表是当前整个html文档，
> 			//当使用document对象调用函数的时候，则表示该函数的作用范围在整个html页面内
> 			
> 			//1.getElementById()   id
> 			//注意：一个id最好只能作用于一个标签
> 			//a.获取指定的标签对象
> 			var input1 = document.getElementById("text1");
> 			//alert(input1);//[object HTMLInputElement]
> 			//b.修改input的值
> 			input1.value = "hello";
> 			
> 			//2.getElementByName()   name
> 			//注意：不管name对应的标签有几个，都会返回一个NodeList
> 			var input2 = document.getElementsByName("input2");
> 			//alert(input2); //[object NodeList]
> 			
> 			//得到的结果为list则通过遍历获取其中的具体的标签对象
> 			for(var i = 0;i < input2.length;i++){
> 				//获取标签对象
> 				var subInput = input2[i];
> 				document.write(subInput.value);
> 			}
> 			
> 			
> 			//3.getElementByClassName()    class
> 			var input3 = document.getElementsByClassName("inputClass");
> 			for(var i = 0;i < input3.length;i++) {
> 				var subInput1 = input3[i];
> 				document.write(subInput1.value);
> 			}
> 			
> 			
> 			//4.getElementByTagName()     tag【标签名称】
> 			var input4 = document.getElementsByTagName("input");
> 			for(var i = 0;i < input4.length;i++) {
> 				var subInput2 = input4[i];
> 				document.write(subInput2.value);
> 			}
> 			
> 			
> 			
> 			//5。特殊情况：如果某个标签只有一个，则采用下面方式获取
> 			var input21 = document.getElementsByName("input2")[0];
> 			var input31 = document.getElementsByClassName("inputClass")[0];
> 			var input41 = document.getElementsByTagName("input")[0];
> 			
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 3.2增加子节点

> 代码演示：
>
> 追加子节点
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<ul>
> 			<li>1111</li>
> 			<li>2222</li>
> 			<li>333</li>
> 			<li>4444</li>
> 		</ul>
> 		
> 		<!--需求：当点击按钮的时候，添加一个li标签-->
> 		<input type="button" onclick="add()" value="添加子节点"/>
> 		
> 		<script>
> 			function add(){
> 				//1.创建文本对象
> 				var textObj = document.createTextNode("5555");
> 				
> 				//2.创建li标签对象
> 				var elementObj = document.createElement("li");
> 				
> 				//3.将文本对象添加到li标签对象，成为的子节点
> 				elementObj.appendChild(textObj);
> 				
> 				//4.获取ul标签对象
> 				var ulElement = document.getElementsByTagName("ul")[0];
> 				
> 				//5.将li标签对象添加到ul标签对象的下面
> 				ulElement.appendChild(elementObj);	
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```
>
> 插入子节点：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<ul>
> 			<li>1111</li>
> 			<li>2222</li>
> 			<!--<li>2.5</li>-->
> 			<li id="li3">333</li>
> 			<li>4444</li>
> 		</ul>
> 		
> 		<input type="button" onclick="add()" value="插入子节点"/>
> 		<script>
> 			function add(){
> 				
> 				//insertBefore:通过父标签进行操作
> 				
> 				//1.创建文本对象
> 				var textObj = document.createTextNode("2.5");
> 				
> 				//2.创建li标签对象
> 				var elementObj = document.createElement("li");
> 				
> 				//3.将文本对象添加到li标签对象，成为的子节点
> 				elementObj.appendChild(textObj);
> 				
> 				//4.获取ul标签对象
> 				var ulElement = document.getElementsByTagName("ul")[0];
> 				
> 				//5.获取指定的标签对象
> 				var li3Element = document.getElementById("li3");
> 				
> 				//6.插入
> 				//注意：指明在哪个父标签对象中的子标签前面插入一个子标签
> 				//参数：新的标签，旧的指定的标签
> 				ulElement.insertBefore(elementObj,li3Element);	
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 3.3删除子节点

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
> 		<ul>
> 			<li>1111</li>
> 			<li id="li2">2222</li>
> 			<li>333</li>
> 			<li>4444</li>
> 		</ul>
> 		<input type="button" onclick="removeLi()" value="删除子节点"/>
> 		<script>
> 			function removeLi(){
> 				
> 				//removeChild() ：注意：需要通过父标签对象进行删除操作
> 				//注意：删除元素节点，属性节点和文本节点会随着被删除
> 				
> 				//1.获取ul标签
> 				var ulElement = document.getElementsByTagName("ul")[0];
> 				
> 				//2.获取需要被删除的标签对象
> 				var li2Element = document.getElementById("li2");
> 				
> 				//3.通过父标签对象删除指定标签对象
> 				ulElement.removeChild(li2Element);
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 3.4替换子节点

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
> 		<ul>
> 			<li>1111</li>
> 			<li>2222</li>
> 			<li id="li3">333</li>
> 			<li>4444</li>
> 		</ul>
> 		<input type="button" onclick="replaceLi()" value="替换子节点"/>
> 		<script>
> 			function replaceLi(){
> 				//repaceChild:注意：必须通过父标签对象进行操作
> 				
> 				//需求：将333的li标签替换为文本为hello的li标签
> 				
> 				//1.创建文本对象
> 				var textObj = document.createTextNode("hello");
> 				
> 				//2.创建li标签对象
> 				var elementObj = document.createElement("li");
> 				
> 				//3.将文本对象添加到li标签对象，成为的子节点
> 				elementObj.appendChild(textObj);
> 				
> 				//4.获取需要被替换的li标签对象
> 				var li3Element = document.getElementById("li3");
> 				
> 				//5.获取ul标签对象
> 				var ulElement = document.getElementsByTagName("ul")[0];
> 				
> 				//6.替换
> 				//参数：新的，旧的
> 				ulElement.replaceChild(elementObj,li3Element);
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 3.5复制节点

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
> 				width: 400px;
> 				height: 400px;
> 				background-color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<ul id="ul">
> 			<li>1111</li>
> 			<li>2222</li>
> 			<li>333</li>
> 			<li>444</li>
> 		<ul/>
> 		<div id="box">
> 	
> 		</div>
> 		
> 		<!--需求：将上面的无需列表复制到div中-->
> 		<script>
> 			//cloneNode()
> 			
> 			//1.获取ul标签对象
> 			var ulElement = document.getElementById("ul");
> 			
> 			//2.执行复制方法，将内容存储到类似剪切板的地方
> 			var copyObj = ulElement.cloneNode(true);
> 			
> 			//3.获取目标标签对象
> 			var divElement = document.getElementById("box");
> 			
> 			//4.将副本添加到目标标签的下面
> 			divElement.appendChild(copyObj);
> 		
> 		</script>
> 		
> 	</body>
> </html>
> 
> ```

##### 3.6属性相关操作

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
> 		<input type="text" name="aaa" id="inputid" value="请输入"/>
> 		<script>
> 			//【了解】
> 			//1.获取标签对象
> 			var inputObj  = document.getElementById("inputid");
> 			
> 			//2.获取属性的值
> 			document.write(inputObj.value);
> 			document.write(inputObj.getAttribute("value"));
> 			
> 			//3.设置某个属性的值
> 			inputObj.value = "hello";
> 			//参数：属性名称  属性的值
> 			inputObj.setAttribute("value","hello");
> 			
> 			//4.创建属性
> 			//var attriObj = document.createAttribute("class");
> 			//原因：属性对象在节点树中也是一个节点的存在【标签节点的子节点】
> 			//inputObj.appendChild(attriObj);
> 			
> 			//5.删除属性
> 			document.write(inputObj.getAttribute("name"));
> 			inputObj.removeAttribute("name");
> 			document.write(inputObj.getAttribute("name"));
> 			
> 			//总结：属性的操作：xxxAttribute（）
> 			//get set create remove
> 		</script>
> 	</body>
> </html>
> ```

##### 3.7Node对象的属性

> nodeName:只读的
>
> ​	元素节点：标签名称
>
> ​	属性节点：属性名称
>
> ​	文本节点：#text
>
> ​	文档节点：#document
>
> nodeValue:
>
> ​	元素节点：undefined或者null
>
> ​	属性节点：属性值
>
> ​	文本节点：文本本身
>
> nodeType:只读的
>
> ​	元素节点：1
>
> ​	属性节点：2
>
> ​	文本节点：3
>
> ​	文档节点：9
>
> 作用：可以根据不同的取值，区分节点的类型
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
> 		<span id="spanid">哈哈哈哈哈哈</span>
> 		<script>
> 			//1.标签节点
> 			var spanObj = document.getElementById("spanid");
> 			document.write(spanObj.nodeName);
> 			document.write(spanObj.nodeValue);
> 			document.write(spanObj.nodeType);
> 			
> 			
> 			//2.属性节点
> 			var idObj = spanObj.getAttributeNode("id");
> 			document.write(idObj.nodeName);
> 			document.write(idObj.nodeValue);
> 			document.write(idObj.nodeType);
> 			
> 			//3.文本节点
> 			//注意：文本节点排列在属性节点的前面
> 			var textObj = spanObj.firstChild;
> 			document.write(textObj.nodeName);
> 			document.write(textObj.nodeValue);
> 			document.write(textObj.nodeType);
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 3.8父节点子节点以及兄弟节点

> parentNode；根据子节点获取父节点
>
> firstChild/lastChild/childNodes；通过父节点获取子节点
>
> nextSibling/previousSibling:兄弟节点/同辈节点
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
> 		<ul id="ulid"><li id="li1">1111</li><li id="li2">2222</li><li id="li3">333</li><li id="li4">4444</li></ul>
> 		<script>
> 			//1.父节点
> 			//a。获取一个已知的子节点
> 			var liObj = document.getElementById("li1");
> 			var ulObj = liObj.parentNode;
> 			
> 			
> 			//2.子节点
> 			//获取ul的父节点对象
> 			var ulElement = document.getElementById("ulid");
> 			var child1 = ulElement.firstChild;
> 			var child2 = ulElement.lastChild;
> 			document.write(child1);//Text
> 			document.write(child2);//Text
> 			
> 			//获取全部的子节点
> 			//注意：返回的是NodeList，获取每个节点对象：遍历
> 			var childs = ulElement.childNodes;
> 			document.write(childs);
> 			document.write(childs.length);
> 			
> 			//存在问题：ul下面有9个子节点，在节点树中，换行符也会被识别成一个文本节点
> 			
> 			
> 			//3.兄弟节点/同辈节点
> 			var li3 = document.getElementById("li3");
> 			var li2 = li3.nextSibling;//document.getElementById("li2");
> 			var li4 = li3.previousSibling;//document.getElementById("li4");
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 3.9innerHTML属性

> innerHTML:获取或者设置节点【标签】的文本值
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
> 				width: 200px;
> 				height: 200px;
> 				background-color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<span id="spanid">hahahahahah</span>
> 		<div id="box">
> 			
> 		</div>
> 		<!--<table border="1"><tr><td>aaaa</td><td>bbbb</td></tr><tr><td>ccc</td><td>dddd</td></tr></table>-->
> 		<script>
> 			//1.获取文本内容
> 			var spanObj = document.getElementById("spanid");
> 			document.write(spanObj.innerHTML);
> 			
> 			
> 			//2.给指定的标签设置文本内容
> 			//2.1设置纯文本
> 			var divObj = document.getElementById("box");
> 			//divObj.innerHTML = "hello";
> 			
> 			//2.2设置html标签
> 			//作用：可以设置纯文本，也可以设置html标签字符串，识别为html标签
> 			divObj.innerHTML = "<table border='1'><tr><td>aaaa</td><td>bbbb</td></tr><tr><td>ccc</td><td>dddd</td></tr></table>";
> 		</script>
> 	</body>
> </html>
> ```

#### 4.事件

> 通过js创建动态网页，事件是可以被js检测到的行为
>
> 注意：网页中的每个元素都可以产生某些触发js函数或者程序的事件

##### 4.1模式

> a.内联模式
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<!--内联模式-->
> 		<!--缺点：没有做到html标签和js代码的分离原则-->
> 		<input type="button" onclick="func();" value="按钮"/>
> 		<input type="button" onclick="alert('hello');"  value="弹出"/>
> 		<script>
> 			function func(){
> 				document.write("hello");
> 			}
> 			//func();
> 		</script>
> 	</body>
> </html>
> ```
>
> b.脚本模式
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body>
> 		<!--脚本模式-->
> 		<input type="button" value="按钮一" />
> 		<input type="button" value="按钮二" />
> 		<script>
> 			//获取第一个input标签对象
> 			var inputObj = document.getElementsByTagName("input")[0];
> 			//添加事件
> 			//给标签对象绑定了一个单击事件，当点击按钮的时候，会触发匿名函数的函数体
> 			inputObj.onclick = function(){
> 				document.write("aaaaa");
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 4.2事件对象

> 事件对象一般被称为event对象，这个对象是浏览器通过函数把这个对象作为参数传递过来
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
> 		<input type="button" value="按钮" />
> 		<script>
> 			function show(){
> 				//全局对象arguments，代表的是参数
> 				document.write(arguments.length);  //0
> 			}
> 			show();
> 			
> 			
> 			var inputObj = document.getElementsByTagName("input")[0];
> 			/*inputObj.onclick = function(){
> 				//在js中，给标签对象绑定事件，事件的触发函数中都有一个隐藏的参数event对象
> 				document.write(arguments.length);   //1
> 			}*/
> 			
> 			
> 			//注意：event只是一个形参【变量名，自定义】
> 			//不一定在所有的事件中都需要将event对象显式的写出来，根据具体的需求决定
> 			inputObj.onclick = function(event){
> 				document.write(event);  //[object MouseEvent]
> 				document.write(arguments.length);   //1
> 				document.write(arguments[0]);
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 4.3鼠标事件

> 所有的时间的组成：on+事件名称
>
> 常用的事件：
>
> ​	onclick:鼠标单击事件
>
> ​	ondbclick:鼠标双击事件
>
> ​	onmousedown:当用户按下鼠标但是还未抬起的时候
>
> ​	onmouseup:当用户抬起鼠标的时候
>
> ​	onmouseover:【hover】，当鼠标移到某个标签的上方的时候
>
> ​	onmouseout:当鼠标移出某个标签上方的时候
>
> ​	onmousemove:当鼠标在某个标签上面移动的时候
>
> ​	onsubmit:表单提交的时候触发【阻止表单提交】
>
> ​	onscroll:鼠标滚动的时候触发
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
> 				width:100px;
> 				height: 100px;
> 				background-color: red;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="box"></div>
> 		<script>
> 			//获取div标签对象
> 			var divObj = document.getElementById("box");
> 			//单击事件
> 			divObj.onclick = function(){
> 				alert("hello");
> 			}
> 			
> 			//双击事件
> 			/*divObj.ondblclick = function(){
> 				alert("hello");
> 			}*/
> 			
> 			//鼠标悬浮
> 			/*divObj.onmouseover = function(){
> 				alert("hello");
> 			}*/
> 			
> 			//鼠标移动
> 			/*divObj.onmousemove = function(){
> 				alert("hello");
> 			}*/
> 			
> 			divObj.onmousedown = function(){
> 				document.write("hello");
> 			}
> 			
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
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			#msg_id{
> 				width: 200px;
> 				height: auto;
> 				background-color: gray;
> 				/*隐藏*/
> 				display: none;
> 				position:absolute;
> 			}
> 			#div1 a{
> 				margin: 30px;
> 				display:inline-block;
> 			}
> 			
> 		</style>
> 	</head>
> 	<body>
> 		<div id="div1">
> 			<a href="#">大娃（红娃）</a><br />
> 			<a href="#">二娃（橙娃）</a><br />
> 			<a href="#">三娃（黄娃）</a><br />
> 			<a href="#">四娃（绿娃）</a><br />
> 			<a href="#">五娃（青娃）</a><br />
> 			<a href="#">六娃（蓝娃）</a><br />
> 			<a href="#">七娃（紫娃）</a><br />
> 			<a href="#">葫芦小金刚</a><br />
> 			<!--显示每个葫芦娃的详细介绍-->
> 			<div id="msg_id"></div>
> 		</div>
> 		<script>
> 			window.onload = function(){
> 				var oDiv = document.getElementById("div1");
> 				var oAs = document.getElementsByTagName("a");
> 				var msgDiv = document.getElementById("msg_id");
> 				
> 				//每个葫芦娃的详细信息
> 				var arrMsg = ["力大无穷，巨大化。(弱点：比较鲁莽，不知随机应变)", "千里眼，顺风耳，灵活聪明，机敏过人，最善于谋划计策(弱点：攻击力与其兄弟相比较过于弱小了，眼睛和耳朵太脆弱)", "铜头铁臂，钢筋铁骨，刀枪不入（弱点：第一部中根本就是没有弱点，但可以以柔克刚降服他。可是到了第二部就被强行加入了一个致命弱点：怕打屁股。性急骄傲）。", "喷火，吸火，霹雳(弱点：受不了激将法，也怕冷)", "吸水，吐水，口吐闪电产生降雨(弱点：水火不相溶，意气用事。第一部中水娃的能力也是没有弱点的，不用吸水也能喷水喷得无穷无尽。到了第二部就变得需要先吸水才能吐水，水量有限。）", "隐身术，透体术，来无影去无踪，聪明机灵，最善于偷盗和行动(弱点：太顽皮。在第一部里能够在被金蛇冰封的情况下透体而出，在第二部前半段能够使用透体术逃出鳄鱼头领爪子的紧紧捉拿，直到被捉的那一下透体术就使不出来了)", "最小，没多大本领，倍受哥哥们的关爱，有宝葫芦，可以吸入魔法、兵器和妖怪，在第一部刚出世时蒙蔽双眼，十分听从妖精的话，把六位哥哥吸进宝葫芦。(弱点:失去宝葫芦，到第二部中宝葫芦那么容易就碎了)", "葫芦娃的合体，七颗葫芦娃的心都溶在他的胸中，七个葫芦娃的本领都长在他的身上，同时也具有七个葫芦娃的弱点。他大闹妖精洞府后，闯入十八层地道，毁掉青蛇精的两件宝物。后变成一座大山，镇压了青蛇精."];
> 
> 				for(var i = 0;i < oAs.length;i++) {
> 					//oAs[i]:每个超链接的对象   arrMsg[i]:每个葫芦娃的详细信息 
> 					//循环的时候，给每一个a标签的位置做一个记录，方便后续可以对应取数组中的数据
> 					oAs[i].index = i;
> 					
> 					//添加事件
> 					//1.移入到a标签的时候，颜色变为橙色，
> 					oAs[i].onmouseover = function(){
> 						//在js中操作css，使用的style属性
> 						//this表示的是当前的a标签对象
> 						this.style.color = "orange";
> 						//将对应的信息显示出来
> 						msgDiv.innerHTML = arrMsg[this.index];
> 						//显示出来
> 						msgDiv.style.display = "block";
> 					}
> 					
> 					//2.当鼠标移出a标签的时候，颜色变回蓝色，将div隐藏
> 					oAs[i].onmouseout = function(){
> 						this.style.color = "blue";
> 						msgDiv.style.display = "none";
> 					}
> 					
> 					//3.当鼠标在a标签上移动的时候，div随着移动
> 					oAs[i].onmousemove = function(event){
> 						
> 						//兼容多种浏览器
> 						//其他的浏览器     ie浏览器
> 						var e = event || window.event;
> 						
> 						msgDiv.style.display = "block";
> 						
> 						//通过事件对象可以获取鼠标在当前页面中的位置，偏移量
> 						
> 						//e.clientX 和e.clientY:鼠标在当前页面中的横纵坐标
> 						msgDiv.style.left = e.clientX + 5 + "px";
> 						msgDiv.style.top = e.clientY + 5 + "px";
> 					}
> 				}
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 4.4拖拽事件

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			.box{
> 				width: 100px;
> 				height: 100px;
> 				background-color: orange;
> 				/*div在整个页面中移动的过程中是参照body的位置*/
> 				position: absolute;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div class="box"></div>
> 		<script>
> 			/*
> 			 * 拖拽事件的实现思路：
> 			 * 1.拖拽触发的条件
> 			 * 	  在元素上有按下的动作之后，才可以拖拽  onmousedowm
> 			 * 2.在移动的过程中
> 			 * 	 计算元素的偏移量
> 			 * 	 将获取到的偏移量赋值给元素的left和top属性
> 			 * 3.拖拽停止的条件:释放资源
> 			 * 	 鼠标抬起   onmouseup
> 			 * 	 onmousemove
> 			 */
> 			
> 			window.onload = function(){
> 				//1.获取div标签对象
> 				var box = document.getElementsByClassName("box")[0];
> 				
> 				//2.添加事件
> 				box.onmousedown = function(event){
> 					//兼容浏览器
> 					var e = event || window.event;
> 					//记录按下的位置在当前元素中的偏移量offset
> 					//偏移量：两点之间的距离
> 					//注意：区别和clientX和clientY【距离原点的距离】
> 					var offsetX = e.offsetX;
> 					var offsetY = e.offsetY;
> 					
> 					//将移动的事件添加给document
> 					document.onmousemove = function(eve){
> 						//获取移动之后鼠标位置
> 						var clientX = eve.clientX;
> 						var clientY = eve.clientY;
> 						
> 						//将停止位置和初始位置之间的差值赋值给left和top属性
> 						box.style.left = clientX - offsetX  + "px";
> 						box.style.top = clientY - offsetY  + "px";	
> 						
> 					}
> 					//解决问题：当鼠标抬起的时候，div将不再移动
> 					document.onmouseup = function(){
> 						//释放资源【移动事件】
> 						document.onmousemove = null;
> 						
> 					}	
> 				}
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 4.5表单事件

> onsubmit:应用在表单中，可以阻止表单的提交【需要提交的内容当不合格的时候】
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
> 		<form id="form" action="#" method="get">
> 			<input type="text" id="user" name="username" placeholder="请输入用户名"/><br />
> 			<input type="submit" value="提交" />
> 		</form>
> 		
> 		<script>
> 			window.onload = function(){
> 				//获取表单对象
> 				var form = document.getElementById("form");
> 				
> 				//校验
> 				//需求：用户名的长度必须在6~10位之间
> 				form.onsubmit = function(){
> 					//获取用户名的标签对象
> 					var user = document.getElementById("user");
> 					if(user.value.length < 6 || user.value.length > 10){
> 						//用户名不合法，则阻止提交
> 						return false;
> 					}else{
> 						//提交
> 					}
> 				}
> 			}
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
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			*{
> 				margin: 0px;
> 				padding: 0px;
> 			}
> 			#box{
> 				position: relative;
> 			}
> 			form{
> 				position: absolute;
> 				top: 100px;
> 				left: 30%;
> 			}
> 			span{
> 				/*初始：将span隐藏*/
> 				display: none;
> 				color: red;
> 				font-size: 12px;
> 			}
> 			input{
> 				margin: 10px;
> 				border: solid 1px black;
> 				border-radius: 1px;
> 				background-color: lightgoldenrodyellow;
> 				height: 25px;
> 				width: 300px;
> 			}
> 			#sub{
> 				position: absolute;
> 				left: 200px;
> 				width: 60px;
> 				border: solid 1px black;
> 				border-radius: 1px;
> 				background-color: lightgoldenrodyellow;
> 				height: 25px;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="box">
> 			<form id="form">
> 				
> 				用户名：&emsp;<input id="user" type="text" placeholder="请输入10个字符以内的用户名"/><span id="userInfo">*用户名格式不正确</span><br />
> 				密码：&emsp;&emsp;<input id="pw" type="password"  placeholder="请输入密码"/><span id="pwInfo">*请包含数字和字母</span><br />
> 				确认密码：<input id="cpw" type="password" placeholder="请确认密码"/><span id="checkPw">*两次输入不一致</span><br />
> 				
> 				&emsp;&emsp;&emsp;&emsp;&emsp;<input type="submit" value="提交" />
> 			</form>
> 		</div>
> 		<script>
> 				var form = document.getElementById("form");
> 				var btn = document.getElementById("sub")
> 				var user = document.getElementById("user")
> 				var pwd = document.getElementById("pw")
> 				var cpwd = document.getElementById("cpw")
> 				var userSpan = document.getElementById("userInfo")
> 				var pwSpan = document.getElementById("pwInfo")
> 				var cpwSpan = document.getElementById("checkPw")
> //				userSpan.style.display = "block"
> 				form.onsubmit = function(){
> 					console.log("进入函数")
> 					if (user.value.length>10||user.value.length<1) {
> 						
> 						userSpan.style.display = "inline-block"
> 						return false;
> 						
> 					} else{
> 							if (pwd.value.length<6||(typeof pwd.value == Number)) {
> 								pwSpan.style.display = "inline-block"
> 								return false;
> 								
> 						} else{
> 								if (pwd.value!=cpwd.value) {
> 									cpwSpan.style.display = "inline-block"
> 									return false;
> 									
> 							} else{
> 								document.write("表单成功提交")
> 							}
> 						}
> 					}
> 				}
> 		</script>
> 	</body>
> </html>
> ```

##### 4.6键盘事件

> 键盘事件：一般情况下键盘事件绑定在document上
>
> 事件分类：
>
> ​	onkeydown:按下键盘上的任意键
>
> ​	onkeyup:抬起键盘上的任意键
>
> ​	onkeypress:按下键盘上的非ctrl/shift/alt/caps lock/numlock功能键
>
> 注意：都会被连续调用
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
> 		<script>
> 			//keyCode:键盘上的各个键在ASCII码表中的对应值
> 			//keydown
> 			document.onkeydown = function(event){
> 				console.log("按下");
> 				
> 				var e = event || window.event;
> 				
> 				//事件对象中的属性
> 				console.log(e.altKey,e.ctrlKey,e.shiftKey,e.keyCode);
> 				
> 			}
> 			
> 			//keyup
> 			document.onkeyup = function(event){
> 				console.log("抬起");
> 				
> 				var e = event || window.event;
> 				
> 				//事件对象中的属性
> 				console.log(e.altKey,e.ctrlKey,e.shiftKey,e.keyCode);
> 			}
> 			
> 			//keypress
> 			document.onkeypress = function(event){
> 				console.log("非功能键");
> 				
> 				var e = event || window.event;
> 				
> 				//事件对象中的属性
> 				console.log(e.altKey,e.ctrlKey,e.shiftKey,e.keyCode);	
> 			}
> 		</script>
> 		
> 	</body>
> </html>
> ```
>
> 应用：
>
> randomColor.js文件
>
> ```javascript
> function randomColor(){
> 	//rgb(255,255,255)   rgba()
> 	var r = parseInt(Math.random() * 256);
> 	var g = parseInt(Math.random() * 256);
> 	var b = parseInt(Math.random() * 256);
> 	
> 	return "rgb(" + r + "," + g + "," + b + ")";
> 	
> }
> ```
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<style>
> 			#box{
> 				width: 200px;
> 				height: 200px;
> 				background-color: red;
> 				position: absolute;
> 			}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="box"></div>
> 		<!--引入js文件-->
> 		<script type="text/javascript" src="js/randomColor.js"></script>
> 		<script>
> 			//1.页面上有一个div，按下shift+c键的改变这个div的颜色【随机】
> 			//2.通过上下左右键控制div的移动
> 			
> 			//需求一
> 			//获取div的标签对象
> 			var box = document.getElementById("box");
> 			document.onkeydown = function(event){
> 				var e = event || window.event;
> 				
> 				//shift + c
> 				if(e.shiftKey == true && e.keyCode == 67){
> 					//修改div的颜色
> 					box.style.backgroundColor = randomColor();
>                 }
> 			}
> 			
> 			//需求二
> 			//事件监听
> 			document.addEventListener("keydown",funcDown,false);
> 			function funcDown(event){
> 				var e = event || window.event;
>                  //根据keyCode的值区分按下的是上下左右哪个键
> 				switch(e.keyCode){
> 					case 37:{
>                       	  //设置移动的举例
> 						box.style.left = box.offsetLeft - 5 + "px";
> 						break;
> 					}
> 					case 38:{
> 						box.style.top = box.offsetTop - 5 + "px";
> 						break;
> 					}
> 					case 39:{
> 						box.style.left = box.offsetLeft + 5 + "px";
> 						break;
> 					}
> 					case 40:{
> 						box.style.top = box.offsetTop + 5 + "px";
> 						break;
> 					}
> 				}
> 			}
> 			
> 		</script>
> 	</body>
> </html>
> ```

##### 4.7事件的传递

> 事件流
>
> ​	描述的是从页面接收的事件的顺序【当几个具有事件的元素重叠在一起的时候，那么你点击其中的一个元素，并不是只有当前这个元素被触发事件，而层叠在这个范围内的元素有可能都会触发事件】
>
> 事件流包含的模式：事件冒泡和事件捕获
>
> ​	事件冒泡：从里向外进行触发
>
> ​	事件捕获：从外向里进行触发
>
> 注意：现代的浏览器都默认采用的是冒泡
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
> 			#box1{width: 200px; height: 200px;background-color: red;}
> 			#box2{width: 100px; height: 100px;background-color: green;}
> 			#box3{width: 50px; height: 50px;background-color: blue;}
> 		</style>
> 	</head>
> 	<body>
> 		<div id="box1">
> 			<div id="box2">
> 				<div id="box3">
> 			
> 				</div>
> 			</div>
> 		</div>
> 		<script>
> 			//获取div标签对象
> 			var div1 = document.getElementById("box1");
> 			var div2 = document.getElementById("box2");
> 			var div3 = document.getElementById("box3");
> 			
> 			//给三个div分别添加监听事件
> 			//true:捕获:从外到内  box1 --->box2 --->box3
> 			//false:冒泡：从内到外   box3 --->box2 --->box1
> 			div1.addEventListener("click",func,false);
> 			div2.addEventListener("click",func,false);
> 			div3.addEventListener("click",func,false);
> 			
> 			function func(){
> 				console.log(this);
> 			}
> 		</script>
> 	</body>
> </html>
> ```

##### 4.8事件的监听

> 事件监听器：
>
> ​	addEventListener();在整个文档中添加监听，可以监听具体是哪种事件被触发了
>
> ​	addEventListener("事件类型",事件需要触发的函数，事件模式【false】)
>
> 注意：
>
> ​	事件类型：直接写事件，去掉on
>
> ​	事件需要触发的函数：函数名称
>
> ​	事件模式：冒泡和捕获，一般采用冒泡
>
> 删除监听
>
> ​	removeEventListener()

#### 5.综合案例

##### 5.1图片轮播

> 代码演示：
>
> html文件
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 		<!--引入css文件-->
> 		<link href="css/style.css" type="text/css" rel="stylesheet" />
> 		
> 	</head>
> 	<body>
> 		<div id="box">
> 			<!--初始图片-->
> 			<img src="img/1.jpg" id="pic" />
> 			<!--显示数字-->
> 			<ul id="list">
> 				<li>1</li>
> 				<li>2</li>
> 				<li>3</li>
> 				<li>4</li>
> 				<li>5</li>
> 				<li>6</li>
> 				<li>7</li>
> 				<li>8</li>
> 			</ul>
> 			<!--左右按钮-->
> 			<div id="left" class="bt">&lt;</div>
> 			<div id="right" class="bt">&gt;</div>
> 		</div>
> 		<!--引入js文件-->
> 		<!--注意：引入外部js文件的时候，因为js文件中需要进行操作标签对象，需要保证在标签加载完毕之后再操作标签-->
> 		<script type="text/javascript" src="js/loopEvent.js"></script>
> 	</body>
> </html>
> ```
>
> css文件
>
> ```css
> *{
> 	padding: 0px;
> 	margin: 0px;
> }
> 
> /*整体效果*/
> #box{
> 	width: 800px;
> 	height: 350px;
> 	margin: 0px auto;
> 	position: relative;
> }
> 
> /*数字列表*/
> #list{
> 	/*取消列表样式*/
> 	list-style: none;
> 	position:absolute;
> 	bottom: 20px;
> 	left:200px;
> }
> 
> /*设置li选项*/
> #list li{
> 	/*浮动*/
> 	float: left;
> 	
> 	width: 20px;
> 	height: 20px;
> 	background-color: lightgray;
> 	
> 	/*削圆角*/
> 	border-radius: 50%;
> 	
> 	/*设置文本居中显示*/
> 	text-align: center;
> 	line-height: 20px;
> 	
> 	/*设置每个li之间有一定的间隔*/
> 	margin-left: 10px;
> }
> 
> /*左右按钮*/
> .bt{
> 	width: 50px;
> 	height: 80px;
> 	background-color: rgba(0,0,0,0.3);
> 	
> 	color: white;
> 	font-size: 30px;
> 	text-align: center;
> 	line-height: 80px;
> 	
> 	position: absolute;
> 	top: 130px;
> 	/*初始状态：隐藏*/
> 	display: none;
> }
> 
> #left{
> 	left:0px;
> }
> #right{
> 	right: 0px;
> }
> ```
>
> js文件
>
> ```javascript
> //1.获取所有的标签对象
> var jsBox = document.getElementById("box");
> var jsPic = document.getElementById("pic");
> var jsLeft = document.getElementById("left");
> var jsRight = document.getElementById("right");
> var jsLiArr = document.getElementsByTagName("li");
> 
> //2.初始状态下，将第一个li设置为红色，表示选中状态
> jsLiArr[0].style.backgroundColor = "red";
> 
> 
> //3.启动一个间歇性定时器，每隔一段时间切换图片
> //定义一个变量，用于记录第几张图片
> var currentPage = 1;
> var timer = setInterval(startLoop,2000);
> function startLoop(){
> 	//当定时器工作起来之后，cureentPage需要改变
> 	currentPage++;
> 	changeImage();
> }
> function changeImage(){
> 	//临界条件的判断
> 	//当图片显示最后一张图片的时候，重新显示第一张图片
> 	if(currentPage == 9){
> 		currentPage = 1;
> 	}
> 	//当图片显示第一张图片的时候，如果点击了左按钮，则重新显示最后一张图片
> 	if(currentPage == 0){
> 		currentPage = 8;
> 	}
> 	
> 	//给img标签重新赋值
> 	jsPic.src = "img/" + currentPage + ".jpg";
> 	
> 	//重新设置小圆点的选中状态
> 	//清除小圆点原有的状态
> 	for(var i = 0; i < jsLiArr.length;i++) {
> 		jsLiArr[i].style.backgroundColor = "lightgray";
> 	}
> 	
> 	//设置当前被选中的小圆点的样式
> 	jsLiArr[currentPage - 1].style.backgroundColor = "red";	
> }
> 
> //4.处理div
> //思路：当鼠标移动到div上的时候，定时器停止，左右按钮显示出来
> //当鼠标移出div的时候，定时器恢复工作，左右按钮隐藏起来
> //鼠标移入
> jsBox.addEventListener("mouseover",overFun,false);
> function overFun(){
> 	//停止定时器
> 	clearInterval(timer);
> 	//左右按钮显示出来
> 	jsLeft.style.display = "block";
> 	jsRight.style.display = "block";
> }
> //鼠标移出
> jsBox.addEventListener("mouseout",outFun,false);
> function outFun(){
> 	//恢复定时器
> 	timer = setInterval(startLoop,2000);
> 	//左右按钮隐藏起来
> 	jsLeft.style.display = "none";
> 	jsRight.style.display = "none";
> }
> 
> //5.左右按钮的事件处理
> //思路：当鼠标进入左右按钮的时候，左右按钮的颜色加深；当鼠标移出左右按钮的时候，颜色恢复
> jsLeft.addEventListener("mouseover",deep,false);
> jsRight.addEventListener("mouseover",deep,false);
> function deep(){
> 	this.style.backgroundColor = "rgba(0,0,0,0.6)";
> }
> jsLeft.addEventListener("mouseout",nodeep,false);
> jsRight.addEventListener("mouseout",nodeep,false);
> function nodeep(){
> 	this.style.backgroundColor = "rgba(0,0,0,0.3)";
> }
> 
> //6.点击左右按钮
> jsLeft.addEventListener("click",function(){
> 	
> 	currentPage--;
> 	
> 	changeImage();
> 	
> },false);
> 
> jsRight.addEventListener("click",function(){
> 	currentPage++;
> 	changeImage();
> 	
> },false);
> 
> //7.处理小圆点的事件
> //思路：当鼠标进入小圆点的时候，直接切换图片，指定的小圆点需要处于选中状态
> for(var i = 0; i < jsLiArr.length;i++) {
> 	//给每个小圆点添加一个标记，用于记录当前是第几个li
> 	jsLiArr[i].index = i + 1;
> 	
> 	//监听每个小圆点
> 	jsLiArr[i].addEventListener("mouseover",function(){
> 		//确定当前是第几张图片
> 		currentPage = parseInt(this.index);
> 		
> 		//切换图片
> 		changeImage();
> 		
> 	},false);
> }
> ```

##### 5.2城市二级关联

> 代码演示：
>
> ```html
> <!DOCTYPE html>
> <html>
> 	<head>
> 		<meta charset="UTF-8">
> 		<title></title>
> 	</head>
> 	<body onload="init()">
> 		<!--省份-->
> 		<!--onchange:当被选中的option选项发生改变的时候，会自动被触发-->
> 		<select id="province" onchange="getCity()">
> 			<option value= 0 >北京</option> 
> 			<option value= 1 >上海</option> 
> 			<option value= 2 >天津</option> 
> 			<option value= 3 >重庆</option> 
> 			<option value= 4 >河北</option> 
> 			<option value= 5 >山西</option> 
> 			<option value= 6 >内蒙古</option> 
> 			<option value= 7 >辽宁</option> 
> 			<option value= 8 >吉林</option> 
> 			<option value= 9 >黑龙江</option> 
> 			<option value= 10 >江苏</option> 
> 			<option value= 11 >浙江</option> 
> 			<option value= 12 >安徽</option> 
> 			<option value= 13 >福建</option> 
> 			<option value= 14 >江西</option> 
> 			<option value= 15 >山东</option> 
> 			<option value= 16 >河南</option> 
> 			<option value= 17 >湖北</option> 
> 			<option value= 18 >湖南</option> 
> 			<option value= 19 >广东</option> 
> 			<option value= 20 >广西</option> 
> 			<option value= 21 >海南</option> 
> 			<option value= 22 >四川</option> 
> 			<option value= 23 >贵州</option> 
> 			<option value= 24 >云南</option> 
> 			<option value= 25 >西藏</option> 
> 			<option value= 26 >陕西</option> 
> 			<option value= 27 >甘肃</option> 
> 			<option value= 28 >宁夏</option> 
> 			<option value= 29 >青海</option> 
> 			<option value= 30 >新疆</option> 
> 			<option value= 31 >香港</option> 
> 			<option value= 32 >澳门</option> 
> 			<option value= 33 >台湾</option>
> 		</select>
> 		<!--城市-->
> 		<select id="city">
> 			
> 		</select>
> 		
> 		<script>
> 			//定义一个数组，保存每个省份的城市信息
> 			var arr = new Array();
> 			arr[0 ]="东城,西城,崇文,宣武,朝阳,丰台,石景山,海淀,门头沟,房山,通州,顺义,昌平,大兴,平谷,怀柔,密云,延庆"; 
> 			arr[1 ]="黄浦,卢湾,徐汇,长宁,静安,普陀,闸北,虹口,杨浦,闵行,宝山,嘉定,浦东,金山,松江,青浦,南汇,奉贤,崇明"; 
> 			arr[2 ]="和平,东丽,河东,西青,河西,津南,南开,北辰,河北,武清,红挢,塘沽,汉沽,大港,宁河,静海,宝坻,蓟县"; 
> 			arr[3 ]="万州,涪陵,渝中,大渡口,江北,沙坪坝,九龙坡,南岸,北碚,万盛,双挢,渝北,巴南,黔江,长寿,綦江,潼南,铜梁,大足,荣昌,壁山,梁平,城口,丰都,垫江,武隆,忠县,开县,云阳,奉节,巫山,巫溪,石柱,秀山,酉阳,彭水,江津,合川,永川,南川"; 
> 			arr[4 ]="石家庄,邯郸,邢台,保定,张家口,承德,廊坊,唐山,秦皇岛,沧州,衡水"; 
> 			arr[5 ]="太原,大同,阳泉,长治,晋城,朔州,吕梁,忻州,晋中,临汾,运城"; 
> 			arr[6 ]="呼和浩特,包头,乌海,赤峰,呼伦贝尔盟,阿拉善盟,哲里木盟,兴安盟,乌兰察布盟,锡林郭勒盟,巴彦淖尔盟,伊克昭盟"; 
> 			arr[7 ]="沈阳,大连,鞍山,抚顺,本溪,丹东,锦州,营口,阜新,辽阳,盘锦,铁岭,朝阳,葫芦岛"; 
> 			arr[8 ]="长春,吉林,四平,辽源,通化,白山,松原,白城,延边"; 
> 			arr[9 ]="哈尔滨,齐齐哈尔,牡丹江,佳木斯,大庆,绥化,鹤岗,鸡西,黑河,双鸭山,伊春,七台河,大兴安岭"; 
> 			arr[10 ]="南京,镇江,苏州,南通,扬州,盐城,徐州,连云港,常州,无锡,宿迁,泰州,淮安"; 
> 			arr[11 ]="杭州,宁波,温州,嘉兴,湖州,绍兴,金华,衢州,舟山,台州,丽水"; 
> 			arr[12 ]="合肥,芜湖,蚌埠,马鞍山,淮北,铜陵,安庆,黄山,滁州,宿州,池州,淮南,巢湖,阜阳,六安,宣城,亳州"; 
> 			arr[13 ]="福州,厦门,莆田,三明,泉州,漳州,南平,龙岩,宁德"; 
> 			arr[14 ]="南昌市,景德镇,九江,鹰潭,萍乡,新馀,赣州,吉安,宜春,抚州,上饶"; 
> 			arr[15 ]="济南,青岛,淄博,枣庄,东营,烟台,潍坊,济宁,泰安,威海,日照,莱芜,临沂,德州,聊城,滨州,菏泽"; 
> 			arr[16 ]="郑州,开封,洛阳,平顶山,安阳,鹤壁,新乡,焦作,濮阳,许昌,漯河,三门峡,南阳,商丘,信阳,周口,驻马店,济源"; 
> 			arr[17 ]="武汉,宜昌,荆州,襄樊,黄石,荆门,黄冈,十堰,恩施,潜江,天门,仙桃,随州,咸宁,孝感,鄂州"; 
> 			arr[18 ]="长沙,常德,株洲,湘潭,衡阳,岳阳,邵阳,益阳,娄底,怀化,郴州,永州,湘西,张家界" 
> 			arr[19 ]="广州,深圳,珠海,汕头,东莞,中山,佛山,韶关,江门,湛江,茂名,肇庆,惠州,梅州,汕尾,河源,阳江,清远,潮州,揭阳,云浮"; 
> 			arr[20 ]="南宁,柳州,桂林,梧州,北海,防城港,钦州,贵港,玉林,南宁地区,柳州地区,贺州,百色,河池"; 
> 			arr[21 ]="海口,三亚"; 
> 			arr[22 ]="成都,绵阳,德阳,自贡,攀枝花,广元,内江,乐山,南充,宜宾,广安,达川,雅安,眉山,甘孜,凉山,泸州"; 
> 			arr[23 ]="贵阳,六盘水,遵义,安顺,铜仁,黔西南,毕节,黔东南,黔南"; 
> 			arr[24 ]="昆明,大理,曲靖,玉溪,昭通,楚雄,红河,文山,思茅,西双版纳,保山,德宏,丽江,怒江,迪庆,临沧"; 
> 			arr[25 ]="拉萨,日喀则,山南,林芝,昌都,阿里,那曲"; 
> 			arr[26 ]="西安,宝鸡,咸阳,铜川,渭南,延安,榆林,汉中,安康,商洛"; 
> 			arr[27 ]="兰州,嘉峪关,金昌,白银,天水,酒泉,张掖,武威,定西,陇南,平凉,庆阳,临夏,甘南" 
> 			arr[28 ]="银川,石嘴山,吴忠,固原"; 
> 			arr[29 ]="西宁,海东,海南,海北,黄南,玉树,果洛,海西"; 
> 			arr[30 ]="乌鲁木齐,石河子,克拉玛依,伊犁,巴音郭勒,昌吉,克孜勒苏柯尔克孜,博尔塔拉,吐鲁番,哈密,喀什,和田,阿克苏"; 
> 			arr[31 ]="香港";
> 			arr[32 ]="澳门"; 
> 			arr[33 ]="台北,高雄,台中,台南,屏东,南投,云林,新竹,彰化,苗栗,嘉义,花莲,桃园,宜兰,基隆,台东,金门,马祖,澎湖";
> 
> 			//初始状态
> 			function init(){
> 				
> 				/*
> 				 * 思路一：
> 				 * var citySelect = 
> 				 * cityArr = arr[0].split(",")
> 				 * for(var  i = 0;i < cityArr.length;i++){
> 				 * 		var optionObj = createElement("option")
> 				 * 		var textObj = createTextNode(cityArr[i])
> 				 * 		optionObj.appendChild(textObj)
> 				 * 		citySelect.appendChild(optionObj)
> 				 * }
> 				 */
> 				
> 				//思路二
> 				//获取city的select标签对象
> 				var city = document.getElementById("city");
> 				var cityArr = arr[0].split(",");
> 				for(var  i = 0;i < cityArr.length;i++){
> 					
> 					//new Option(str1,str2):一般用于动态生成选择项目
> 					//<option value="str2">str1</option>
> 					//select标签：其中有多少个option标签，编号，类似于数组的使用
> 					city[i] = new Option(cityArr[i],cityArr[i]);
> 				}	
> 			}
> 			
> 			
> 			//改变状态
> 			function getCity(){
> 				//获取省份和城市的select标签对象
> 				var province = document.getElementById("province");
> 				var city = document.getElementById("city");
> 				
> 				//获取当前选中的省份
> 				var index = province.selectedIndex;
> 				
> 				//获取对应的城市
> 				var cityArr = arr[index].split(",");
> 				
> 				//每个省份下面的城市的数量是不相同的，所以对应的option选项的个数也是不相同的
> 				city.length = 0;
> 				
> 				for(var  i = 0;i < cityArr.length;i++){
> 					
> 					city[i] = new Option(cityArr[i],cityArr[i]);
> 				}	
> 				
> 			}
> 
> 		</script>
> 	</body>
> </html>
> ```

​	

​				

​			

