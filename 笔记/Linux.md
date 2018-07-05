### 一、Linux系统简介

#### 1.Linux发展史

> 1946年世界上的第一台计算机就产生了，刚产生出的计算机并没有操作系统，需要手工输入
>
> 人机矛盾:1. 只能一个人使用  2.人工速度慢于计算
>
> 产生操作系统（根据人的需求产生）
>
> 1965年麻省理工，ATT，贝尔实验室去研发一套操作系统，想要允许300台操作并使用
>
> 1969年实现进度缓慢，计划失败了
>
> 1969-1970 肯.汤姆逊移植了一个软件，定制一套标准，Unix系统
>
> 1970 推出了Unix系统，Unix系统元年，操作系统元年，电脑底层时间 1970
>
> 1985 年推出了windows
>
> Unix是一个传统的美国人思维，按年，按月，或者按设备收美金
>
> 林纳斯.托瓦兹看不惯Unix
>
> 1991年模拟Unix写了一套操作系统Linux
>
> 开源，当时也只有大约100开发者，核心开发者大约5人
>
> 1993年Linux使用者大约10w数量级

#### 2.Linux的应用领域

> IT服务器Linux、Unix、Windows三分天下，Linux系统可谓后起之秀，特别是最近几年来，服务器端Linux操作系统不断地扩大市场份额，且每年增长势头迅猛，并且开始对Windows及Unix服务器市场的地位构成严重的威胁。Linux占80%左右（包括CentOS,Ubuntu等），Windows占12.8%,solaris占6.2%。可见，在未来的服务器领域市场里Linux是大势所趋。
>
> Linux作为企业级服务器的应用十分广泛，利用Linux系统可以为企业架构WWW服务器、数据库服务器、负载均衡服务器、邮件服务器、DNS服务器、代理服务器、路由器等，不但使企业降低了运营成本，同时还获得了Linux系统带来的高稳定性和高可靠性，且无须考虑商业软件的版权问题
>
> Linux操作系统应用的三大领域
>
> a.企业级服务器应用领域【利用Linux系统可以为企业架构WWW服务器、数据库服务器、负载均衡服务器、邮件服务器、DNS服务器、代理服务器、路由器等，不但使企业降低了运营成本，同时还获得了Linux系统带来的高稳定性和高可靠性，且无须考虑商业软件的版权问题，随着Linux在服务器领域的广泛应用，近几年来，该系统已经参透到电信、金融、政府、教育、银行、石油等各个行业，同时各大硬件厂商也相继支持Linux操作系统。这一切表明，Linux在服务器市场前景光明。同时，大型、超大型互联网企业都在使用Linux系统作为其服务器端的程序运行平台，全球及国内排名前十的网站使用的几乎都是Linux系统，Linux已经逐步渗透到了各个领域的企业里】
>
> b.嵌入式Linux系统应用领域【由于Linux系统开放源代码，功能强大、可靠、稳定性强、灵活而且具有极大的伸缩性，再加上它广泛支持大量的微处理体系结构、硬件设备、图形支持和通信协议，因此，在嵌入式应用的领域里，从因特网设备（路由器、交换机、防火墙，负载均衡器）到专用的控制系统（自动售货机，手机，PDA，各种家用电器），LINUX操作系统都有很广阔的应用市场。特别是经过这几年的发展，它已经成功地跻身于主流嵌入式开发平台。例如《在智能手机领域，Android Linux已经在智能手机开发平台牢牢地占据了一席之地。嵌入式系统应用领域是另一个应用领域】
>
> c.个人桌面Linux应用领域【所谓个人桌面系统，其实就是我们在办公室使用的个人计算机系统，例如：Windows xp、windows 7、Mac等。Linux系统在这方面的支持也已经非常好了，完全可以满足日常的办公需求】
>
> 服务器、云计算、嵌入式、政府、企业、影视、超算、桌面

#### 3.Linux的特点

> 开放
> 多用户
> 多任务
> 出色的速度性能
> 良好的用户界面
> 丰富的网络功能
> 可靠的系统安全
> 良好的移植性
> 具有标准兼容性

#### 4.系统的使用

> ​	严格来讲，Linux不是一个操作系统，Linux只是一个操作系统中的内核。内核是什么？内核建立了计算机软件与硬件之间通讯的平台，内核提供系统服务，比如文件管理、虚拟内存、设备I/O等。
>
> ​	既然Linux只是一个内核。那么我们通常所说的Linux操作系统又是什么？我们通常所说的Linux，指 GNU/Linux ，即采用Linux内核的GNU操作系统。是的，操作系统的实际名称是GNU。什么是GNU？GNU代表GNU’s Not Unix。可以说是一个操作系统又可以说是一种规范
>
> 参考资料：https://blog.csdn.net/baidu_32134295/article/details/52439823

#### 5.Linux组成

> Linux内核:
> ​	操作系统的心脏，运行程序和管理硬件设备的核心程序
> Linux Shell:
> ​	系统的用户界面，提供用户与内核进行交互操作的一种接口
> Linux 文件系统:
> ​	文件存储在磁盘等存储设备上的组织方法
> Linux 应用程序
> ​	标准的程序集，比如文本编辑，编程语言，Window，办公套件，Internet工具，数据库等

#### 6.Linux版本

> RedHat ：性能稳定，老牌的linux发行版。收费的是RedHat Enterprise Linux（RHEL,redhat的企业版）
>
> Fedora  ：界面比较好看，RedHat的社区免费版，非常强大。
>
> Centos  ：可以算是RHEL的克隆版，但它最大的好处是免费
> SUSE  ：德国最著名的linux发行版
>
> Debian：算是迄今为止最遵循GUN规范的linux系统（GUN的目标就是创建一套完全自由的操作系统）
>
> Ubuntu  ：Debian的后继或是一个分支，对于初学者而言比较友好
>
> Ubuntu的优点：
>
> ​	a.简便易用，对于初学者，Ubuntu系统算是非常简单的了
>
> ​	b.版本更新定期而频繁，每六个月就有一个新的ubuntu版本
>
> ​	c.使用者非常多，支持的社区也很多
>
> ​	d.标准化	

#### 7.Linux VS Windows

> 见图

### 二、环境安装

#### 1.VMWare安装

> 虚拟机：寄宿在物理机中的一类特殊的软件【特殊之处在于：可以当做操作系统使用】

#### 2.Ubuntu系统安装

> 【可能会出现的问题】
>
> 1.CPU 不支持虚拟化，如下图：
>
> 
>
> ```
> 解决办法：
> https://jingyan.baidu.com/article/b24f6c82c11ad286bfe5da23.html
> 
> BIOS：全称(Base  Input  Output System)，中文是基本输入输出系统
> 虽然BIOS成百上千，但功能都是一样的，对硬件信息进行保存设置，所以设置方法上也大同小异，90%以上的电脑设置方法都差不多，进入BIOS按键也就那几个<del，Esc，F1，F2，F8，F9，F10，F11，F12>
> 
> 英文：Press Esc to enter SETUP
> 中文：按Esc键进入BIOS设置
> 
> 英文：Press F2 go to Setup Utility
> 中文：按F2去设置BIOS实用程序
> 
> 英文：Press DEL to enter EFI BIOS SETUP
> 中文：按Del键进入EFI模式的BIOS进行设置
> 
> 英文：Press Del run Setup
> 中文：按Del键运行BIOS设置
> 
> 英文：Press F1 run Setup
> 中文：按F1键运行BIOS设置
> 
> 英文：Press <F2> to Setup
> 中文：按F2进行BIOS设置
> 
> 【t400进入bios的方法:按f1】
> 1.首先需要确定计算机型号和菜谱，BIOS(基本输入输出系统)系统型号，因为过老的计算机是不支持虚拟机化的
> 2.检测方式：
> 	开机时按 F2，F12，DEL,ESC 等键就可以进到 BIOS[至于按哪个 看电脑品牌]
> 3.进入 BIOS 后，找到 Configuration 选项或者 Security选项， 然后选择 Virtualization或者 Intel Virtual Technology 就可以开始操作了
> 4.然后回车 将其设置为 Enabled
> 5.保存 BIOS 设置重启计算机
> 6.进入操作系统 右键 选择任务管理器 - 性能 - CPU - 查看虚拟化设置(已启动表示设置成功了， 可以装虚拟机了)
> ```
>
> 不同型号的电脑进入bios的按键总结：
>
> 见图

#### 3.VMWare Tools安装

> 作用：保证两个系统之间可以进行文件共享
>
> 步骤：
>
> ​	虚拟机/找到当前虚拟机右键点击 —> 安装 vmware tools 选项 —> 光盘出现 —>双击打开 ——> 双击vmwaretoiso —> 将其中的内容拖至桌面 —> 进入文件夹 ——> 右击在终端打开 —> 
>
> ​	命令：
>
> ​		./wmware-install.pl [回车]
>
> ​		权限不够
>
> ​		更改命令：
>
> ​		sudo ./wmware-install.pl
>
> ​		输入密码  【回车】
>
> ​		提示 no  —> 输入 yes
>
> ​		之后一直按照提示回车 遇到 yes 输入 yes即可
>
> ​		安装完成系统重启

### 三、系统设置

#### 1.外观

#### 2.账户和密码

##### 3.主机名，终端用户名和密码

> 用户分为两类：
>
> ​	普通用户，超级管理员【root用户】
>
> ​	root用户时系统中唯一的超级管理员，它具有等同于操作系统的权限
>
> ​	普通用户也可以调用超级管理员的指令

##### 3.1修改root用户密码

> ```
> 演示命令：
> rock@rockrong:~$ su root
> 密码： 			#输入yangyang0122认证失败
> su：认证失败
> rock@rockrong:~$ su root 
> 密码： 		     #输入rock1204
> root@rockrong:/home/rock# passwd root
> 输入新的 UNIX 密码： 
> 重新输入新的 UNIX 密码： 
> passwd：已成功更新密码
> root@rockrong:/home/rock# reboot
> ```

##### 3.2修改主机名

> ```
> 演示命令：
> rock@rockrong:~$ su root
> 密码： 
> root@rockrong:/home/rock# vim /etc/hostname      
> root@rockrong:/home/rock# vim /etc/hosts
> root@rockrong:/home/rock# reboot
> ```

##### 3.3修改用户名

> ```
> 演示命令：
> rock@yangyang-virtualmachine:~$ pwd
> /home/rock
> rock@yangyang-virtualmachine:~$ su root
> 密码： 
> root@yangyang-virtualmachine:/home/rock# vim /etc/shadow
> root@yangyang-virtualmachine:/home/rock# cd ..
> root@yangyang-virtualmachine:/home# ls
> rock
> root@yangyang-virtualmachine:/home# mv rock yangyang
> root@yangyang-virtualmachine:/home# ls
> ```

### 上堂回顾

> 1.ajax
>
> ​	作用：客户端【浏览器】与服务器进行异步交互
>
> ​	使用：
>
> ​		原生：步骤【创建核心对象XMLHTTPrequest，连接open，发送请求send，处理响应onreadystatechange】
>
> ​			get和post：get需要将发送的内容拼接在url中，post将发送的内容需要通过请求体发送
>
> ​		第三方库：jQuery
>
> ​			对象.load:加载html页面
>
> ​			$.getScript:加载js文件
>
> ​			$.get和$.post:全局函数，封装了原生的ajax请求，
>
> ​			$.ajax:$.get和$.post的总体，可以进行get请求和post请求
>
> 1. Linux
>
>    系统设置

### 四、目录结构

#### 1.Windows文件系统

> 看到的是一个个驱动器盘符，例如：C盘，D盘等
>
> 每个驱动器都有自己的根目录结构，形成了树结构

#### 2.Linux文件系统

> ubuntu没有盘符这个概念，只有一个根目录 ：/,所有目录和文件都存放在/的下面
>
> 注意：在Linux系统下所有的内容都被视为文件，目录也被视为文件
>
> ```
> ls -l       #查看当前路径下文件的详细信息
> ls -l  /     #查看根目录下的详细信息
> ```
>
> ```python
> Linux目录结构： 
> 
> / ： 根目录     #Linux下的根目录有且只有一个，在终端输入/home,就是告诉电脑，从根目录开始，进入home目录
> /boot : boot配置文件、内核和其它启动时所需的文件
> /etc ：存放系统配置有关的文件   #用户信息都存放在etc目录下【修改用户名和密码】
> /home ：存放普通用户目录      #ls /home/   列出home下所有的普通用户
> /mnt ：硬盘上手动挂载的文件系统	
> 	#挂载：把硬盘连接在文件系统上【类似于大卡车车厢挂载在车头上】
> 	#注意：默认是空的
> /media ：自动挂载（加载）的硬盘分区以及类似CD、数码相机等可移动介质。	
> /cdrom ：挂载光盘 
> /opt ： 存放一些可选程序,如某个程序测试版本,安装到该目录的程序的所有数据,库文件都存在同个目录下
> /root ： 系统管理员的目录，对于系统来说，系统管理员好比上帝
> 	#可以对系统做任何的操作，比如删除文件，一般情况下尽量少使用root用户
>   	#可以通过命令使得普通用户享有root用户的权限
> /bin ：存放常用的程序文件      #binary，二进制文件或者命令文件
> /sbin ：系统管理命令，这里存放的是系统管理员使用的管理程序 
> /tmp ：临时目录，存放临时文件   #temp，暂时的，临时目录，
> 	#注意：是一些命令或者程序产生的一些临时文件，系统会定期清理该目录下的文件
> /usr ：在这个目录下，你可以找到那些不适合放在/bin或/etc目录下的额外的工具。比如游戏、打印工具等。/usr目录包含了许多子目录： 
> 	/usr/bin目录用于存放程序;
> 	/usr/share用于存放一些共享的数据，比如音乐文件或者图标等等;
> 	/usr/lib目录用于存放那些不能直接 运行的，但却是许多程序运行所必需的一些函数库文件。
> 	/usr/local ： 这个目录一般是用来存放用户自编译安装软件的存放目录；一般是通过源码包安装的软件，如果没有特别指定安装目录的话，一般是安装在这个目录中。
> 	/usr/bin/ 非必要可执行文件 (在单用户模式中不需要)；面向所有用户。
> 	/usr/include/ 标准包含文件。
> 	/usr/lib/ /usr/bin/和/usr/sbin/中二进制文件的库。
> 	/usr/sbin/ 非必要的系统二进制文件，例如：大量网络服务的守护进程。
> 	/usr/share/ 体系结构无关（共享）数据。
> 	/usr/src/ 源代码,例如:内核源代码及其头文件。
> 	/usr/X11R6/ X Window系统 版本 11, Release 6.
> 	/usr/local/ 本地数据的第三层次，具体到本台主机。通常而言有进一步的子目录， 例如：bin/、lib/、share/.
> 
> /var ：该目录存放那些经常被修改的文件，包括各种日志、数据文件；
>     /var/cache/ 应用程序缓存数据。这些数据是在本地生成的一个耗时的I/O或计算结果。应用程序必须能够再生或恢复数据。缓存的文件可以被删除而不导致数据丢失。
>     /var/lib/ 状态信息。 由程序在运行时维护的持久性数据。 例如：数据库、包装的系统元数据等。
>     /var/lock/ 锁文件，一类跟踪当前使用中资源的文件。
>     /var/log/ 日志文件，包含大量日志文件。
>     /var/mail/ 用户的电子邮箱。
>     /var/run/ 自最后一次启动以来运行中的系统的信息，例如：当前登录的用户和运行中的守护进程。现已经被/run代替[13]。
>     /var/spool/ 等待处理的任务的脱机文件，例如：打印队列和未读的邮件。
>     /var/spool/mail/ 用户的邮箱(不鼓励的存储位置)
>     /var/tmp/ 在系统重启过程中可以保留的临时文件。
>     
> /lib : 目录是根文件系统上的程序所需的共享库，存放了根文件系统程序运行所需的共享文件。这些文件包含了可被许多程序共享的代码，以避免每个程序都包含有相同的子程序的副本，故可以使得可执行文件变得更小，节省空间。
> /lib32 : 同上
> /lib64 ： 同上
> /lost+found ： 该目录在大多数情况下都是空的。但当突然停电、或者非正常关机后，有些文件就临时存放在；
> /dev : 存放设备文件
> /run ：代替/var/run目录，
> /proc : 虚拟文件系统，可以在该目录下获取系统信息，这些信息是在内存中由系统自己产生的，该目录的内容不在硬盘上而在内存里；
> 	cat /proc/cpuinfo
> 	
> /sys ： 和proc一样，虚拟文件系统，可以在该目录下获取系统信息，这些信息是在内存中由系统自己产生的，该目录的内容不在硬盘上而在内存里；
> ```
>
> 补充：
>
> ```
> .   代表当前目录
> ..  代表上一级目录
> 注意：根目录下.和..都代表当前目录
> 
> 相对路径和绝对路径
> 相对路径：从当前位置开始描述的路径
> 绝对路径：从/目录开始描述的路径
> ```

> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ ls -l
> 总用量 40
> drwxr-xr-x 3 yangyang rock 4096 6月  26 02:23 Desktop
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Documents
> drwxr-xr-x 2 yangyang rock 4096 3月  25 22:05 Downloads
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Music
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Pictures
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Public
> drwxrwxr-x 3 yangyang rock 4096 3月  25 22:43 PycharmProjects
> drwxrwxr-x 3 yangyang rock 4096 3月  25 22:37 Software
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Templates
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Videos
> yangyang@yangyang-virtualmachine:~$ pwd
> /home/yangyang
> yangyang@yangyang-virtualmachine:~$ ls -l /
> 总用量 100
> drwxr-xr-x   2 root root  4096 3月  25 22:26 bin
> drwxr-xr-x   3 root root  4096 6月  26 18:01 boot
> drwxrwxr-x   2 root root  4096 7月  18  2017 cdrom
> drwxr-xr-x  19 root root  4020 6月  26 18:01 dev
> drwxr-xr-x 137 root root 12288 6月  26 18:10 etc
> drwxr-xr-x   3 root root  4096 6月  26 17:58 home
> lrwxrwxrwx   1 root root    33 3月  25 22:28 initrd.img -> boot/initrd.img-4.13.0-37-generic
> yangyang@yangyang-virtualmachine:~$ ls /mnt/
> 
> yangyang@yangyang-virtualmachine:~$ pwd
> /home/yangyang
> yangyang@yangyang-virtualmachine:~$ cd Desktop/     
> yangyang@yangyang-virtualmachine:~/Desktop$ cd .
> yangyang@yangyang-virtualmachine:~/Desktop$ cd ..
> yangyang@yangyang-virtualmachine:~$ cd /home/yangyang/Desktop/   #绝对路径
> yangyang@yangyang-virtualmachine:~/Desktop$ cd ..
> yangyang@yangyang-virtualmachine:~$ cd Desktop/      #相对路径
> yangyang@yangyang-virtualmachine:~/Desktop$
> ```

### 五、快捷键

> ```
> ctrl + shift +  + :放大字体，放大终端窗口
> ctrl + -   :缩小字体
> 
> ctrl  +  alt:显示鼠标
> 
> ctrl + alt + t :快速打开终端
> 
> tab  :命令行自动补全
> 
> 箭头上下键：翻看已经执行过的命令
> 
> ctrl + f :前进一个字符
> ctrl + b：后退一个字符
> ctrl + a:回到行首
> ctrl + e:回到行尾
> 
> ctrl + w: 向左删除一个单词
> ctrl + u:向左删除全部单词
> ctrl + k:向右删除全部单词
> 
> ctrl + y:将ctrl + w，ctrl + u，ctrl + k删除的结果恢复
> 
> ctrl + l:清屏【并不是真正意义上的清屏，只是将历史记录向上翻一页】
> 
> ctrl + c:中断执行
> 
> ctrl + d:退出终端
> ```

### 六、安装软件

#### 1.apt

> 软件管理 apt ( Advanced Packaging Tool ) , 他可以自动下载、配置、安装软件包
>
> ```
> apt-cache search package 搜索包
> apt-cache show package 获取包的相关信息，如说明、大小、版本等
> sudo apt-get install package 安装包
> sudo apt-get install package –reinstall 重新安装包
> sudo apt-get -f install 强制安装
> sudo apt-get remove package 删除包
> sudo apt-get remove package –purge 删除包，包括删除配置文件等
> sudo apt-get autoremove 自动删除不需要的包
> sudo apt-get update 更新源
> sudo apt-get upgrade 更新已安装的包
> sudo apt-get dist-upgrade 升级系统
> sudo apt-get dselect-upgrade 使用 dselect 升级
> apt-cache depends package 了解使用依赖
> apt-cache rdepends package 了解某个具体的依赖
> sudo apt-get build-dep package 安装相关的编译环境
> apt-get source package 下载该包的源代码
> sudo apt-get clean && sudo apt-get autoclean 清理下载文件的存档
> sudo apt-get check 检查是否有损坏的依赖
> ```
>
> apt的配置文件
>
> ```
> /etc/apt/sources.list 设置软件包的获取来源
> /etc/apt/apt.conf apt配置文件
> /etc/apt/apt.conf.d apt的零碎配置文件
> /etc/apt/preferences 版本参数
> /var/cache/apt/archives/partial 存放正在下载的软件包
> /var/cache/apt/archives 存放已经下载的软件包
> /var/lib/apt/lists 存放已经下载的软件包详细信息
> /var/lib/apt/lists/partial 存放正在下载的软件包详细信息
> ```

#### 2.dpkg

> dpkg是Debian软件包管理器的基础，被用于安装、卸载和供给和.deb软件包相关的信息,dpkg本身是一个底层的工具，本身并不能从远程包仓库下载包以及处理包的依赖的关系，需要将包从远程下载后再安装
>
> ```
> dpkg -i package.deb 安装包
> dpkg -r package 删除包
> dpkg -P package 删除包（包括配置文件）
> dpkg -L package 列出与该包关联的文件
> dpkg -l package 显示该包的版本
> dpkg –unpack package.deb 解开 deb 包的内容
> dpkg -S keyword 搜索所属的包内容
> dpkg -l 列出当前已安装的包
> dpkg -c package.deb 列出 deb 包的内容
> dpkg –configure package 配置包
> ```

### 七、常用命令

#### 1.概述

> 语法：
>
> command    options    parameters
>
> command    :命令名称
>
> options    ：选项，可以对命令进行控制，根据具体需求可写可不写
>
> parameters：传给命令的参数，根据具体需求可写可不写，也可以写多个

#### 2.查看帮助文档

> 1>--help
>
>  作用：Linux命令自带的帮助信息
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ ls --help
> yangyang@yangyang-virtualmachine:~$ cd --help
> ```

> 2>man
>
> 作用：相当于一个手册，包含了大多数的命令以及命令的使用方式
>
> ```python
> man命令中常用的按键
> 空格键		向下翻页
> 上下方向键    向上或者向下翻一行
> fn + 左方向键		回到首页
> fn + 右方向键       回到尾页
> 
> /xxx       从上到下进行搜索和指定关键字有关的内容
> ?xxx	  从上到下进行搜索和指定关键字有关的内容
> n	      定位到下一个搜索到的关键字
> N		  定位到上一个搜索到的关键字
> q		  退出帮助文档
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ man ls 
> ```

> 3>history   查看执行过的命令
>
> 当系统执行过一些命令之后，可以通过上下键翻看以前的命令，history将执行过的命令列举出来
>
> history   显示最近1000条记录
>
> history   5   显示最后5条命令
>
> !number    number 是history每条命令前面的编号，直接使用表示执行对应的命令
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ history        #显示最近1000条记录
> yangyang@yangyang-virtualmachine:~$ history  5     #显示最后5条命令
>   958  cd ..
>   959  ls
>   960  pwd
>   961  history 
>   962  history  5
> yangyang@yangyang-virtualmachine:~$ !951            #指定编号对应的命令
> cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ 
> ```

> 补充：
>
> ```python
> #查看历史命令的记录
> #命令不会一直保存下去，最多只会显示1000条，查看信息：
> 演示命令：
> angyang@yangyang-virtualmachine:~/Desktop$ cat ~/.bashrc | grep -i hist
> # don't put duplicate lines or lines starting with space in the history.
> HISTCONTROL=ignoreboth
> # append to the history file, don't overwrite it
> shopt -s histappend
> # for setting history length see HISTSIZE and HISTFILESIZE in bash(1)
> HISTSIZE=1000        #最多显示的条数
> HISTFILESIZE=2000		#执行过的命令都会存放在一个文件中，这个文件中最多存放2000条
> alias alert='notify-send --urgency=low -i "$([ $? = 0 ] && echo terminal || echo error)" "$(history|tail -n1|sed -e '\''s/^\s*[0-9]\+\s*//;s/[;&|]\s*alert$//'\'')"'
> ```
>
> ```python
> #查看命令保存的位置
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ ls -a ~/.bash*
> /home/yangyang/.bash_history         #存放历史命令的文件
> /home/yangyang/.bashrc				#存放详细信息的文件
> /home/yangyang/.bash_logout          #存放日志的文件
> yangyang@yangyang-virtualmachine:~/Desktop$ gedit /home/yangyang/.bash_history         #打开文件
> yangyang@yangyang-virtualmachine:~/Desktop$ 
> ```

#### 3.文件管理

> 1>ls:列举出当前工作目录的内容【list】
>
> ```python
> -a 用于显示所有文件和子目录(包括隐藏文件)
> -A 同-a，但不列出“.”(表示当前目录)和“..”(表示当前目录的父目录)
> -l 除了文件名之外，还将文件的权限、所有者、文件大小等信息详细列出来。 (文件大小是字节)
> -lh 与-l 类似  只不过文件大小显示的是 KB [默认是按照文件名的 abcd 排序的]
> -lht 与-l -lh 类似  排序是按照修改时间降序排的
> -lhtr 按照时间升序排
> -r 将目录的内容清单以英文字母顺序的逆序显示
> -t 按文件修改时间进行排序
> -F 在列出的文件名和目录名后添加标志。例如，在可执行文件后添加“*”，在目录名后添加“/”以区分不同的类型
> -R 如果目标目录及其子目录中有文件，就列出所有的文件
> 
> 补充
> drwxr-xr-x 2 yangyang rock 4096 6月   5 21:41 Desktop
> 一、文件类型
> #第一位代表的是文件类型：
> 	- 代表是文件
> 	d 代表目录
>     b 块设备文件
>     c  字符设备文件
>     l  链接文件
>     p  管道文件
>     s  socket文件
> 
> 二、文件权限
> #第二位到十位是文件的权限
> 权限共九位，分三组，每三个一组
> 	rwx		
> 	r  read  可读权限，可以用数字4表示
> 	w  write   可写权限，可以用数字2表示
> 	x  execute	可执行权限，可以用数字1表示
> 	-  表示没有相应权限，可以用数字0表示
> 	
> 三、文件和目录的权限类型	
> 对于文件而言：
> 	可读权限表示允许读其内容，禁止对其做任何的更改操作
> 	可写权限表示可以修改编辑文件的内容或者删除文件（要有文件所在目录的写权限）
> 	可执行表示允许将文件作为一个程序执行
> 
> 对目录而言：
> 	可读权限表示允许显示该目录中的内容
> 	可写权限表示可以在该目录中新建，删除，重命名文件
> 	可执行权限表示可以进入该目录，可执行是基本权限，如果没有它，就进不了目录	
>         
> 四、硬链接的个数
> #第二列一位代表硬链接的个数
> 	取值范围为0-7
> 	-0  代表什么权限都没有
> 	-1	文件只能执行
> 	-2	文件只有写权限
> 	-3	文件可写可执行
> 	-4	只读权限
> 	-5	可读可执行
> 	-6	可读可写
> 	-7 可读可写可执行
> 	
> 五、表示组
> #第三列表示组
> 	分三个组：
> 	代表当前用户的权限[user]
> 	代表用户所属组的权限[group]
> 	代表其他组的权限[other]
> ```

> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ ls
> Desktop    Downloads  Pictures  PycharmProjects  Templates
> Documents  Music      Public    Software         Videos
> yangyang@yangyang-virtualmachine:~$ ls /home/yangyang
> Desktop    Downloads  Pictures  PycharmProjects  Templates
> Documents  Music      Public    Software         Videos
> yangyang@yangyang-virtualmachine:~$ ls Desktop/
> vmware-tools-distrib            VNC-Server-6.1.1-Linux-x64.deb
> VNC-6.1.1-Linux-x64-DEB.tar.gz
> yangyang@yangyang-virtualmachine:~$ ls -a
> .                   Documents      .mysql_history    .sogouinput
> ..                  Downloads      .nano             .sudo_as_admin_successful
> .apport-ignore.xml  .gconf         .pam_environment  .sunpinyin
> .bash_history       .gnome         Pictures          Templates
> .bash_logout        .gnupg         .pki              Videos
> .bashrc             .ICEauthority  .presage          .viminfo
> .cache              .java          .profile          .virtualenvs
> .compiz             .lesshst       Public            .vnc
> .config             .local         .PyCharm2017.3    .Xauthority
> .dbus               .mozilla       PycharmProjects   .xinputrc
> Desktop             Music          .python_history   .xsession-errors
> .dmrc               .mysql         Software          .xsession-errors.old
> yangyang@yangyang-virtualmachine:~$ ls -A
> .apport-ignore.xml  .java             .python_history
> .bash_history       .lesshst          Software
> .bash_logout        .local            .sogouinput
> .bashrc             .mozilla          .sudo_as_admin_successful
> .cache              Music             .sunpinyin
> .compiz             .mysql            Templates
> .config             .mysql_history    Videos
> .dbus               .nano             .viminfo
> Desktop             .pam_environment  .virtualenvs
> .dmrc               Pictures          .vnc
> Documents           .pki              .Xauthority
> Downloads           .presage          .xinputrc
> .gconf              .profile          .xsession-errors
> .gnome              Public            .xsession-errors.old
> .gnupg              .PyCharm2017.3
> .ICEauthority       PycharmProjects
> yangyang@yangyang-virtualmachine:~$ ls -l
> 总用量 40
> drwxr-xr-x 3 yangyang rock 4096 6月  26 02:23 Desktop
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Documents
> drwxr-xr-x 2 yangyang rock 4096 3月  25 22:05 Downloads
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Music
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Pictures
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Public
> drwxrwxr-x 3 yangyang rock 4096 3月  25 22:43 PycharmProjects
> drwxrwxr-x 3 yangyang rock 4096 3月  25 22:37 Software
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Templates
> drwxr-xr-x 2 yangyang rock 4096 7月  18  2017 Videos
> yangyang@yangyang-virtualmachine:~$ ls -h
> Desktop    Downloads  Pictures  PycharmProjects  Templates
> Documents  Music      Public    Software         Videos
> yangyang@yangyang-virtualmachine:~$ ls -r
> Videos     Software         Public    Music      Documents
> Templates  PycharmProjects  Pictures  Downloads  Desktop
> yangyang@yangyang-virtualmachine:~$ ls -t
> Desktop          Software   Documents  Pictures  Templates
> PycharmProjects  Downloads  Music      Public    Videos
> yangyang@yangyang-virtualmachine:~$ ls -F
> Desktop/    Downloads/  Pictures/  PycharmProjects/  Templates/
> Documents/  Music/      Public/    Software/         Videos/
> yangyang@yangyang-virtualmachine:~$ ls -R
> .:
> Desktop    Downloads  Pictures  PycharmProjects  Templates
> Documents  Music      Public    Softw
> ```

> 2>pwd	查看当前的工作目录[print working directory]
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ pwd
> /home/yangyang
> ```

> 3>查看文件
>
> ```python
> cat：查看完整的文件内容        ********
> 	-n	:显示每一行的行号，包括空行
> 	-b	:显示每一行的行号，不包括空行
> #使用文件内容较少的情况下使用cat
> head：查看文件内容
> tail：查看文件内容
> 
> less：查看文件
> more：查看文件
> #使用文件内容较少的情况下使用more
> 
> wc：一次显示文件行数，字节数以及文件名信息
> stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的时间，stat命令的输出信息比ls命令还要详细
> file：查看文件的类型
> echo：用于在终端输出字符串或变量的值
> 
> |:管道，作用：将一个命令的输出作为另一个命令的输入，格式：命令1 | 命令2  ****
> >：输出重定向，Linux允许将执行结果重定向到一个文件，本应显示在终端上的内容保存到指定文件中     #清空源文件
> >>：输出重定向，Linux允许将执行结果重定向到一个文件，本应显示在终端上的内容保存到指定文件中 
> 1>  标准正确输出，同上
> 1>> 标准正确输出，同上     #追加不清空
> 2> 标准错误输出，同上
> 2>> 标准错误输出，同上
> &> 标准正确输出和标准错误输出，同上
> 	将1和2结合在一起了
>   
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> aaa.txt               VNC-6.1.1-Linux-x64-DEB.tar.gz
> vmware-tools-distrib  VNC-Server-6.1.1-Linux-x64.deb
> yangyang@yangyang-virtualmachine:~/Desktop$ cat aaa.txt 
> hfuiewhg
> less：查看文件
> head：查看文件内容
> tail：查看文件内容
> less：查看文件
> more：查看文件
> wc：一次显示文件行数，字节数以及文件名信息
> stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的时间，stat命令的输出信息比ls命令还要详细
> file：查看文件的类型
> echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ cat -n aaa.txt 
>      1	hfuiewhg
>      2	less：查看文件
>      3	head：查看文件内容
>      4	tail：查看文件内容
>      5	less：查看文件
>      6	more：查看文件
>      7	wc：一次显示文件行数，字节数以及文件名信息
>      8	stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的时间，stat命令的输出信息比ls命令还要详细
>      9	file：查看文件的类型
>     10	echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ cat -b aaa.txt 
>      1	hfuiewhg
>      2	less：查看文件
>      3	head：查看文件内容
>      4	tail：查看文件内容
>      5	less：查看文件
>      6	more：查看文件
>      7	wc：一次显示文件行数，字节数以及文件名信息
>      8	stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的时间，stat命令的输出信息比ls命令还要详细
>      9	file：查看文件的类型
>     10	echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ head aaa.txt 
> hfuiewhg
> less：查看文件
> head：查看文件内容
> tail：查看文件内容
> less：查看文件
> more：查看文件
> wc：一次显示文件行数，字节数以及文件名信息
> stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的时间，stat命令的输出信息比ls命令还要详细
> file：查看文件的类型
> echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ head -2 aaa.txt 
> hfuiewhg
> less：查看文件
> yangyang@yangyang-virtualmachine:~/Desktop$ tail aaa.txt 
> hfuiewhg
> less：查看文件
> head：查看文件内容
> tail：查看文件内容
> less：查看文件
> more：查看文件
> wc：一次显示文件行数，字节数以及文件名信息
> stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的时间，stat命令的输出信息比ls命令还要详细
> file：查看文件的类型
> echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ tail -2 aaa.txt 
> file：查看文件的类型
> echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ less aaa.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ more aaa.txt 
> hfuiewhg
> less：查看文件
> head：查看文件内容
> tail：查看文件内容
> less：查看文件
> more：查看文件
> wc：一次显示文件行数，字节数以及文件名信息
> stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的
> 时间，stat命令的输出信息比ls命令还要详细
> file：查看文件的类型
> echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ wc aaa.txt 
>  10  10 421 aaa.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ stat aaa.txt 
>   文件：'aaa.txt'
>   大小：421       	块：8          IO 块：4096   普通文件
> 设备：801h/2049d	Inode：572338      硬链接：1
> 权限：(0644/-rw-r--r--)  Uid：( 1000/yangyang)   Gid：( 1000/    rock)
> 最近访问：2018-06-27 11:35:53.174601466 +0800
> 最近更改：2018-06-27 11:34:31.286596606 +0800
> 最近改动：2018-06-27 11:34:31.290596607 +0800
> 创建时间：-
> yangyang@yangyang-virtualmachine:~/Desktop$ file aaa.txt 
> aaa.txt: UTF-8 Unicode text
> yangyang@yangyang-virtualmachine:~/Desktop$ echo "today is a good day"
> today is a good day
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> aaa.txt               VNC-6.1.1-Linux-x64-DEB.tar.gz
> vmware-tools-distrib  VNC-Server-6.1.1-Linux-x64.deb
> yangyang@yangyang-virtualmachine:~/Desktop$ ls > bbb.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ cat aaa.txt 
> hfuiewhg
> less：查看文件
> head：查看文件内容
> tail：查看文件内容
> less：查看文件
> more：查看文件
> wc：一次显示文件行数，字节数以及文件名信息
> stat：查看文件详细信息，可以获取文件的文件名、大小、权限，最近访问以及最近更改的时间，stat命令的输出信息比ls命令还要详细
> file：查看文件的类型
> echo：用于在终端输出字
> yangyang@yangyang-virtualmachine:~/Desktop$ cat aaa.txt > bbb.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ 
> ```

> 4>tree       以树形结构去显示目录结构
>
> ​	注意：默认情况下是当前路径下的所有文件的显示
>
> ​	
>
> ```python
> -d 	只显示文件夹
> -f	显示文件的完整路径
> -L 2	：只看前两级的内容
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$  tree
> yangyang@yangyang-virtualmachine:~/Desktop$  tree -d
> yangyang@yangyang-virtualmachine:~/Desktop$  tree -f 
> yangyang@yangyang-virtualmachine:~/Desktop$  tree -L 2
> ```

> 5>cd	切换工作目录【change  diretory】
>
> ```python
> 用法：cd  路径[此处可以是相对路径，也可以是绝对路径]       ******
> 特殊用法： 
> cd	切换到当前用户的主目录，用户登录的时候，默认的目录就是用户的主目录
> cd ~	切换到当前用户的主目录
> cd .	切换到当前目录
> cd ..	切换到上一级目录			*******
> cd - 	返回上一次切换的目录
> cd #	回到当前用户的主目录
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ cd /home/yangyang
> yangyang@yangyang-virtualmachine:~$ cd
> yangyang@yangyang-virtualmachine:~$ cd ~
> yangyang@yangyang-virtualmachine:~$ cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ cd -
> /home/yangyang
> yangyang@yangyang-virtualmachine:~$ cd Desktop/
> ```

> 6>mv	移动或者重命名文件或者目录
>
> 注意：如果目标是文件，则表示重命名
>
> ​	   如果目标是目录，则表示移动
>
> ```python
> 命令格式：mv [参数] 源文件  [目标路径|目标文件名]    ------》可以cd到【文件所在路径下】或者【直接通过路径指明文件】
> -i	在目标文件存在的时候会询问是否要覆盖
> -b	当目标文件存在的时候，不会进行询问直接覆盖
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ mv aaa.txt  abc.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ mv bbb.txt bbb1.txt  bbb2.txt  dir1/
> yangyang@yangyang-virtualmachine:~/Desktop$ mv -i abc.txt  dir1/
> mv：是否覆盖'dir1/abc.txt'？ y
> yangyang@yangyang-virtualmachine:~/Desktop$ mv -b abc.txt  dir1/
> ```

> 7>cp	复制文件或者目录
>
> ```python
> 命令格式：cp [参数] 源文件 目标文件
> 
> -i	在目标文件存在的时候会询问是否要覆盖【交互式复制】
> -r 若给出的源文件是一目录文件，此时cp将递归复制该目录下所有的子目录和文件。此时目标文件必须为一个目录名
> -a 复制的时候保持文件原有属性
> -f 对于已经存在的目标文件不提示
> -v 显示拷贝进度
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ cp -i  abc.txt  dir1/
> cp：是否覆盖'dir1/abc.txt'？ n      #交互式复制
> yangyang@yangyang-virtualmachine:~/Desktop$ cp dir1 dir2/
> cp: 略过目录'dir1'
> yangyang@yangyang-virtualmachine:~/Desktop$ cp dir1 dir2
> cp: 略过目录'dir1'
> yangyang@yangyang-virtualmachine:~/Desktop$ cp -r  dir1 dir2/
> yangyang@yangyang-virtualmachine:~/Desktop$ cp -v  abc.txt dir2/
> 'abc.txt' -> 'dir2/abc.txt'
> ```

> 8>创建文件或者目录
>
> ```python
> 8.1>mkdir	创建一个新的目录   【make directory】
> 	-p：创建出具有嵌套层关系的文件目录
> 8.2>touch	创建空白文件，可以设置文件的时间
> 	名词解释：
> 	atime:最后一次访问文件或目录的时间【access time】
> 	mtime：最后一次修改内容的时间【modify time】
> 	ctime ：最后一次改变属性的时间【change time】
> 	参数：
> 	-a   修改atime
> 	-m	修改mtime
> 	-c	修改ctime
> 	-d	同时修改atime与mtime
> 	-t	同时修改atime与mtime，格式{YYYYMMDDhhmm}
> 	注意：只有-d和-t后面可以指定时间，其他的只能把时间修改为当前时间
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ mkdir check   #创建单层目录
> yangyang@yangyang-virtualmachine:~/Desktop$ mkdir -p a/b/c/d  #创建多级目录
> yangyang@yangyang-virtualmachine:~/Desktop$ mkdir -p b/{c,d}/{e,f,g}
> yangyang@yangyang-virtualmachine:~/Desktop$ touch file1.txt  
> yangyang@yangyang-virtualmachine:~/Desktop$ touch -m file2.txt
> ```

> 9>删除文件或者目录
>
> ```python
> 9.1>rmdir  删除给定的目录,注意：只能删除空文件夹
> 9.2>rm	删除文件或者目录，可以删除一个目录中的一个或多个文件或目录，也可以将某个目录及其下面所有子文件和目录都删掉
> 
> 	-r	删除目录，否则删不掉
> 	-ri	交互式删除，每次删除都会进行询问
> 	-rf	强制删除文件或目录
> 
> 演示命令：
> angyang@yangyang-virtualmachine:~/Desktop$ rmdir check
> yangyang@yangyang-virtualmachine:~/Desktop$ rmdir b
> rmdir: 删除 'b' 失败: 目录非空
> yangyang@yangyang-virtualmachine:~/Desktop$ rm -r dir1
> yangyang@yangyang-virtualmachine:~/Desktop$ rm -ri dir2
> rm：是否进入目录'dir2'? y          #交互式删除
> rm：是否进入目录'dir2/dir1'? y
> rm：是否删除普通文件 'dir2/dir1/bbb1.txt'？ y
> rm：是否删除普通文件 'dir2/dir1/abc.txt'？ ^C     #control + c中断执行
> yangyang@yangyang-virtualmachine:~/Desktop$ rm -rf a       #强制删除目录
>   yangyang@yangyang-virtualmachine:~/Desktop$ rm -rf file1.txt #强制删除文件
> ```

> 10>ln         建立链接文件
>
> 注意：建立链接文件相当于windows上创建一个快捷方式
>
> 分类：
>
> ​	软链接：不占用磁盘空间的，源文件删除则软连接失效【-s】
>
> ​	硬链接：可以占用磁盘空间，源文件删除对硬链接没有影响，
>
> ​		注意：只能链接普通文件，不能链接目录
>
> ```python
> 演示命令：
> #软连接
> yangyang@yangyang-virtualmachine:~/Desktop$ rm -rf *
> yangyang@yangyang-virtualmachine:~/Desktop$ touch a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ll
> 总用量 8
> drwxr-xr-x  2 yangyang rock 4096 6月  27 15:19 ./
> drwxr-xr-x 31 yangyang rock 4096 6月  27 14:35 ../
> -rw-r--r--  1 yangyang rock    0 6月  27 15:19 a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ln -s a.txt a
> yangyang@yangyang-virtualmachine:~/Desktop$ ll
> 总用量 8
> drwxr-xr-x  2 yangyang rock 4096 6月  27 15:21 ./
> drwxr-xr-x 31 yangyang rock 4096 6月  27 14:35 ../
> lrwxrwxrwx  1 yangyang rock    5 6月  27 15:21 a -> a.txt
> -rw-r--r--  1 yangyang rock    0 6月  27 15:19 a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt 
> fhuwegjawhg
> hello
> html
> linux
> fjeehdgjsehdg
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a
> fhuwegjawhg
> hello
> html
> linux
> fjeehdgjsehdg
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt 
> fhuwegjawhg
> hello
> html
> linux
> fjeehdgjsehdg
> 462527568357628
> yangyang@yangyang-virtualmachine:~/Desktop$ rm a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a
> cat: a: 没有那个文件或目录
> 
> #硬链接
> yangyang@yangyang-virtualmachine:~/Desktop$ touch a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ rm a
> yangyang@yangyang-virtualmachine:~/Desktop$ ln a.txt a
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt 
> hfijehgwahg
> hgjehgjwagd
> hjaehdg
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a
> hfijehgwahg
> hgjehgjwagd
> hjaehdg
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt 
> hfijehgwahg
> hgjehgjwagd
> hjaehdg
> 64723882
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a
> hfijehgwahg
> hgjehgjwagd
> hjaehdg
> 64723882
> yangyang@yangyang-virtualmachine:~/Desktop$ ll
> 总用量 16
> drwxr-xr-x  2 yangyang rock 4096 6月  27 15:27 ./
> drwxr-xr-x 31 yangyang rock 4096 6月  27 14:35 ../
> -rw-r--r--  2 yangyang rock   41 6月  27 15:28 a
> -rw-r--r--  2 yangyang rock   41 6月  27 15:28 a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ rm a.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a
> hfijehgwahg
> hgjehgjwagd
> hjaehdg
> 64723882
> 
> 【总结】
> 对于软连接而言，如果软连接和源文件不在同一个目录下，则原文件使用绝对路径，不能使用相对路径
> 对于硬链接而言，两个文件占用相同大小的磁盘空间，如果源文件被删除，硬链接不受任何影响，正常使用
> 软连接是常见的形式
> ```

> 11>grep	      文本搜索
>
> ```python
> 强大的文本搜索工具，grep允许对文本文件进行模式查找，如果找到匹配模式，grep打印包含模式的所有行
> 注意：搜索内容串可以是正则表达式
> 
> -c：返回匹配到的数目
> -i：忽略大小写	
> -n：显示匹配行以及行号
> -v：反向选择，列出没有关键词的行【求反】
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ touch a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ touch a1.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ touch a2.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> a  a1.txt  a2.txt  a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ls | grep a1.txt
> a1.txt								#以ls的输出作为grep的输入
> yangyang@yangyang-virtualmachine:~/Desktop$ ls | grep a
> a									#检索桌面上文件名中包含a的文件
> a1.txt
> a2.txt
> a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ touch b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> a  a1.txt  a2.txt  a.txt  b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ls | grep a
> a
> a1.txt
> a2.txt
> a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ls | grep -c a
> 4
> yangyang@yangyang-virtualmachine:~/Desktop$ ls | grep -n a
> 1:a
> 2:a1.txt
> 3:a2.txt
> 4:a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ls | grep -v a
> b.txt									#反向检索【否定】
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt 
> yuieqwhfije
> fhhjeanf
> hfjaehdgj
> hello
> 
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt | grep a
> fhhjeanf								#检索a.txt文件中包含a的内容
> hfjaehdgj
> ```

> 12>which  查找其他命令所在的位置
>
> 注意：显示其他指定命令的路径
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ which ls
> /bin/ls
> yangyang@yangyang-virtualmachine:~/Desktop$ which cd
> yangyang@yangyang-virtualmachine:~/Desktop$ which cat
> /bin/cat
> yangyang@yangyang-virtualmachine:~/Desktop$ which pwd
> /bin/pwd
> yangyang@yangyang-virtualmachine:~/Desktop$ which ll
> 
> #注意：如果是封装的命令，查找不到位置，比如上面的cd和ll
> ```

> 13>type   寻找命令所在的位置，包括命令别名
>
> ```python
> -a：可以找到所有，包括别名和位置
> 
> #type和which的区别：type列出别名和位置，which列出位置
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ type ls
> ls 是 `ls --color=auto' 的别名
> yangyang@yangyang-virtualmachine:~/Desktop$ type -a ls
> ls 是 `ls --color=auto' 的别名
> ls 是 /bin/ls
> ```

> 14>find	  按照指定条件来查找文件
>
> ```python
> 格式：find  【查找路径】 【查找方式】 【查找条件】
> 
> -name：匹配名称，默认是精确匹配
> -size：匹配文件大小
> -atime  -n  +n：匹配访问内容的时间（-n指n天以内，+n指n天以前）
> -empty
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> a  a1.txt  a2.txt  a.txt  b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ find -name a1.txt
> ./a1.txt								#查找文件名为a1.txt的文件
> yangyang@yangyang-virtualmachine:~/Desktop$ find -size 1k
> ./a.txt									#查找文件大小等于1k的文件
> ./a
> yangyang@yangyang-virtualmachine:~/Desktop$ find -size +1k
> . 									   #查找文件大小大于1k的文件
> yangyang@yangyang-virtualmachine:~/Desktop$ find -size -1k
> ./b.txt        							#查找文件大小小于1k的文件
> ./a2.txt
> ./a1.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ find -empty     #查找空文件
> ./b.txt
> ./a2.txt
> ./a1.txt
> ```

> 15>locate   查找数据
>
> ```python
> -i:忽略大小写
> -c：不输出寻找结果，仅计算找到的文件数量
> -l：仅输出指定的几行，  例如：-l 8，输出8行
> -r：后面可以接正则表达式
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ locate hello
> /boot/grub/i386-pc/hello.mod				#全局查找包含hello的内容
> /usr/lib/grub/i386-pc/hello.mod
> /usr/lib/python2.7/__phello__.foo.py
> /usr/lib/python2.7/__phello__.foo.pyc
> /usr/lib/python3.5/__phello__.foo.py
> /usr/lib/python3.5/__pycache__/__phello__.foo.cpython-35.pyc
> /usr/share/doc/python3-uno/demo/hello_world_comp.py
> /usr/share/doc/python3-xlsxwriter/docs/_static/hello01.png
> /usr/share/doc/syslinux-common/asciidoc/hello.txt
> /usr/share/locale-langpack/en@boldquot/LC_MESSAGES/hello.mo
> /usr/share/locale-langpack/en@quot/LC_MESSAGES/hello.mo
> /usr/share/locale-langpack/en_AU/LC_MESSAGES/hello.mo
> /usr/share/locale-langpack/en_CA/LC_MESSAGES/hello.mo
> /usr/share/locale-langpack/en_GB/LC_MESSAGES/hello.mo
> /usr/share/locale-langpack/zh_CN/LC_MESSAGES/hello.mo
> yangyang@yangyang-virtualmachine:~/Desktop$ locate /etc/sh
> /etc/shadow
> /etc/shadow-
> /etc/shells
> ```

> 16>sort    给文件内容排序
>
> ```python
> -f：忽略大小写的差异，例如 A 与 a 视为编码相同；
> -b：忽略最前面的空格符部分；
> -n：使用『纯数字』进行排序(默认是以文字型态来排序的)；
> -r：反向排序；
> -u：就是 uniq，表示唯一的，相同的数据中，仅出现一行代表；
> -t：分隔符，默认是用 [tab] 键来分隔；
> -k：以那个区间 (field) 来进行排序的意思
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt
> yuieqwhfije
> fhhjeanf
> hfjaehdgj
> hello
> 
> yangyang@yangyang-virtualmachine:~/Desktop$ sort a.txt
> 									#默认按照升序排序
> fhhjeanf
> hello
> hfjaehdgj
> yuieqwhfije
> yangyang@yangyang-virtualmachine:~/Desktop$ sort -t ":" -k 2 a.txt
> 									#以：为分隔符，按照指定区间排序
> hfj:aehd:gj
> fhhj:ean:f
> hello:fhedg:fhjdg
> yuieq:whfij:e
> ```

> 17>cut       可以从一个文本文件或者文本流中提取文本列
>
> ```python
> -d ：后面接分隔字符。与 -f 一起使用；
> -f ：依据 -d 的分隔字符将一段信息分割成为数段，用 -f 取出第几段的意思；
> -c ：以字符 (characters) 的单位取出固定字符区间；( -连接区间  ,取的是和的意思)
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a.txt
> yuieq:whfij:e
> fhhj:ean:f
> hfj:aehd:gj
> hello:fhedg:fhjdg
> 
> yangyang@yangyang-virtualmachine:~/Desktop$ cut -d ":" -f 1 a.txt
> yuieq								#提取以：为分隔符的第1个区间的数据
> fhhj		
> hfj
> hello
> 
> yangyang@yangyang-virtualmachine:~/Desktop$ cut -c 1 a.txt
> y									#提取第一个字符
> f
> h
> h
> 
> yangyang@yangyang-virtualmachine:~/Desktop$ cut -c 1,3 a.txt
> yi									#提取第1个和第3个字符
> fh
> hj
> hl
> 
> yangyang@yangyang-virtualmachine:~/Desktop$ cut -c 1-3 a.txt
> yui									#提取第1到第3个字符
> fhh
> hfj
> hel
> ```

> 18>tee    读取标准输入的数据，并将其内容输出成文件【向指定文件中写入内容】
>
> ```python
> -a：读取原文件内容，并追加新的内容,如果不设置该选项，则新的内容直接覆盖旧的内容
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ tee a.txt 
> ^C
> yangyang@yangyang-virtualmachine:~/Desktop$ tee -a a.txt
> fhajhf								#向指定文件中追加内容
> fhajhf
> gjfg
> gjfg
> jghqj
> jghqj
> gjrgh
> gjrgh
> ^C
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a1.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ tee a1.txt
> tuwit								#向指定文件中写入内容
> tuwit
> grehwjgh
> grehwjgh
> ^C
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a1.txt
> tuwit		
> grehwjgh
> yangyang@yangyang-virtualmachine:~/Desktop$ tee a1.txt a2.txt
> uuuu								#向多个指定文件中写入内容
> uuuu
> ppppp
> ppppp
> ^C
> ```

> 19>gedit	打开Linux下的文本编辑器
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ gedit      #打开一个新的文本文件
> yangyang@yangyang-virtualmachine:~/Desktop$ gedit a1.txt	#打开一个现有的文本文件
> ```

### 上堂回顾

> 1.目录结构
>
> ​	/；根目录
>
> ​	/home:存放普通用户
>
> ​	/etc:存放系统配置的文件【用户信息，用户密码，root密码等】
>
> ​	/root:存放超级管理员
>
> ​	/tmp:临时目录，存放临时文件
>
> 2.常用命令
>
> ​	文件管理：
>
> ​	ls:列出指定目录下的所有的信息
>
> ​		-a:包括隐藏文件
>
> ​		-l:权限，大小，文件属性等全部列出来
>
> ​		ls -a -l ----->ls -al ----->ll
>
> ​	pwd:查看当前的工作目录
>
> ​	cat:查看文件的内容
>
> ​		cat  finename
>
> ​	cd：切换工作目录
>
> ​		cd  指定的路径【相对路径，绝对路径】
>
> ​		cd  ..      退回上一级目录
>
> ​		cd  ../..
>
> ​		cd  .    当前路径
>
> ​	mv：移动，重命名
>
> ​		mv   源文件   目标文件   ：重命名
>
> ​		mv   源文件   目标目录 ：移动
>
> ​	cp:复制
>
> ​		cp  源文件   目标目录：
>
> ​		cp 源目录   目标目录：
>
> ​	mkdir:创建目录       -p
>
> ​	touch:创建空白文件
>
> ​	rmdir:删除空目录
>
> ​	rm:删除目录和文件
>
> ​		-r:
>
> ​		-rf:强制性删除
>
> ​	ln:建立链接文件
>
> ​		软连接：ln -s   源文件  链接
>
> ​		硬链接：ln  源文件  链接
>
> ​	grep:检索
>
> ​	find:按照条件查找文件
>
> ​	tee:输入

### 八、常用命令

#### 1.文件管理

> 20>sed      流编辑器，一次处理一行内容，主要用来自动编辑一个或多个文件
>
> ```
> 格式：[-nefr] [动作] [文件]
> 
> 选项：
> -e<script>或--expression=<script>：以选项中的指定的script来处理输入的文本文件；
> -f<script文件>或--file=<script文件>：以选项中指定的script文件来处理输入的文本文件；
> -h或--help：显示帮助；
> -n或--quiet或——silent：仅显示script处理后的结果；
> -V或--version：显示版本信息。
> 
> 参数：
> 文件：指定待处理的文本文件列表。
> 
> 命令：
> a\ 在当前行下面插入文本。
> i\ 在当前行上面插入文本。
> c\ 把选定的行改为新的文本。
> d 删除，删除选择的行。
> D 删除模板块的第一行。
> s 替换指定字符
> h 拷贝模板块的内容到内存中的缓冲区。
> H 追加模板块的内容到内存中的缓冲区。
> g 获得内存缓冲区的内容，并替代当前模板块中的文本。
> G 获得内存缓冲区的内容，并追加到当前模板块文本的后面。
> l 列表不能打印字符的清单。
> n 读取下一个输入行，用下一个命令处理新的行而不是用第一个命令。
> N 追加下一个输入行到模板块后面并在二者间嵌入一个新行，改变当前行号码。
> p 打印模板块的行。
> P(大写) 打印模板块的第一行。
> q 退出Sed。
> b lable 分支到脚本中带有标记的地方，如果分支不存在则分支到脚本的末尾。
> r file 从file中读行。
> t label if分支，从最后一行开始，条件一旦满足或者T，t命令，将导致分支到带有标号的命令处，或者到脚本的末尾。
> T label 错误分支，从最后一行开始，一旦发生错误或者T，t命令，将导致分支到带有标号的命令处，或者到脚本的末尾。
> w file 写并追加模板块到file末尾。  
> W file 写并追加模板块的第一行到file末尾。  
> ! 表示后面的命令对所有没有被选定的行发生作用。  
> = 打印当前行号码。  
> # 把注释扩展到下一个换行符以前。  
> 
> sed替换标记
> g 表示行内全面替换。  
> p 表示打印行。  
> w 表示把行写入一个文件。  
> x 表示互换模板块中的文本和缓冲区中的文本。  
> y 表示把一个字符翻译为另外的字符（但是不用于正则表达式）
> \1 子串匹配标记
> & 已匹配字符串标记
> 
> sed元字符集
> ^ 匹配行开始，如：/^sed/匹配所有以sed开头的行。
> $ 匹配行结束，如：/sed$/匹配所有以sed结尾的行。
> . 匹配一个非换行符的任意字符，如：/s.d/匹配s后接一个任意字符，最后是d。
> * 匹配0个或多个字符，如：/*sed/匹配所有模板是一个或多个空格后紧跟sed的行。
> [] 匹配一个指定范围内的字符，如/[ss]ed/匹配sed和Sed。  
> [^] 匹配一个不在指定范围内的字符，如：/[^A-RT-Z]ed/匹配不包含A-R和T-Z的一个字母开头，紧跟ed的行。
> \(..\) 匹配子串，保存匹配的字符，如s/\(love\)able/\1rs，loveable被替换成lovers。
> & 保存搜索字符用来替换其他字符，如s/love/**&**/，love这成**love**。
> \< 匹配单词的开始，如:/\<love/匹配包含以love开头的单词的行。
> \> 匹配单词的结束，如/love\>/匹配包含以love结尾的单词的行。
> x\{m\} 重复字符x，m次，如：/0\{5\}/匹配包含5个0的行。
> x\{m,\} 重复字符x，至少m次，如：/0\{5,\}/匹配至少有5个0的行。
> x\{m,n\} 重复字符x，至少m次，不多于n次，如：/0\{5,10\}/匹配5~10个0的行。
> ```

> ```python
> #1.增加
> #a,追加，a后面可以接字符串，但是注意：新接的字符串会出现在下一行
> yangyang@yangyang-virtualmachine:~$ cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> a  a1.txt  a2.txt  a.txt  b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ vim a1.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ sed  "/^text/a\pppppp" a1.txt 
> this is a test
> text
> pppppp
> hello
> uuuu
> ppppp
> yangyang@yangyang-virtualmachine:~/Desktop$ sed -i "2a\python1805" a1.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ vim a1.txt 
> 
> 
> #i,插入，和a之间的区别在于添加到了匹配到的行的前面
> yangyang@yangyang-virtualmachine:~/Desktop$ sed  "/^text/i\pppppp111" a1.txt 
> this is a test
> pppppp111
> text
> python1805
> hello
> uuuu
> ppppp
> 
> #2.删除
> #d,删除，注意：所有d后面不接任何内容
> yangyang@yangyang-virtualmachine:~/Desktop$ sed "3d" a1.txt 
> this is a test
> text
> hello
> uuuu
> ppppp
> yangyang@yangyang-virtualmachine:~/Desktop$ sed "1,3d" a1.txt 
> hello
> uuuu
> ppppp
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a1.txt 
> this is a test
> text
> python1805
> hello
> uuuu
> ppppp
> yangyang@yangyang-virtualmachine:~/Desktop$ sed "1d;3d;5d" a1.txt
> text
> hello
> ppppp
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a1.txt 
> this is a test
> text
> python1805
> hello
> uuuu
> ppppp
> 
> #3.替换
> #s 
> yangyang@yangyang-virtualmachine:~/Desktop$ sed "s/text/exam/" a1.txt
> this is a test
> exam
> python1805
> hello
> uuuu
> ppppp
> yangyang@yangyang-virtualmachine:~/Desktop$ cat a1.txt 
> this is a test
> ```

> 21>打包和压缩
>
> 打包：将一大堆的文件或者目录变成一个总的文件
>
> 压缩：将一个较大的文件处理成一个较小的文件
>
> 操作：先打包【tar命令】-----》压缩【gzip命令和bzip2等】
>
> a.tar     可以把一大堆的文件和目录全部打包成一个文件
>
> ```python
> -A或--catenate：新增文件到已存在的备份文件；
> -B：设置区块大小；-c或--create：建立新的备份文件；
> -C <目录>：这个选项用在解压缩，若要在特定目录解压缩，可以使用这个选项。
> -d：记录文件的差别；
> -x或--extract或--get：从备份文件中还原文件；
> -z或--gzip或--ungzip：通过gzip指令处理备份文件；
> -Z或--compress或--uncompress：通过compress指令处理备份文件；
> -f<备份文件>或--file=<备份文件>：指定备份文件；
> -v或--verbose：显示指令执行过程；
> -r：添加文件到已经压缩的文件；
> -u：添加改变了和现有的文件到已经存在的压缩文件；
> -j：支持bzip2解压文件；
> -v：显示操作过程；
> -l：文件系统边界设置；
> -k：保留原有文件不覆盖；
> -m：保留文件不被覆盖；
> -w：确认压缩文件的正确性；
> -p或--same-permissions：用原来的文件权限还原文件；
> -P或--absolute-names：文件名使用绝对名称，不移除文件名称前的“/”号；
> -N <日期格式> 或 --newer=<日期时间>：只将较指定日期更新的文件保存到备份文件里；
> --exclude=<范本样式>：排除符合范本样式的文件。
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ ls
> a  a1.txt  a2.txt  a.txt  b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ tar -cvf log.tar a1.txt
> a1.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ rm -rf log.tar
> yangyang@yangyang-virtualmachine:~/Desktop$ tar -zcvf log.tar.gz a1.txt 
> a1.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ rm  -rf log.tar.gz 
> yangyang@yangyang-virtualmachine:~/Desktop$ tar -jcvf log.tar.bz2 a1.txt
> a1.txt
> 
> 总结：
> -cvf:直接打包，但是不压缩
> -zcvf:.tar.gz代表的是使用gzip压缩的包
> -jcvf:.tar.bz2代表的是使用bzip2压缩的包
> ```
>
> b.gzip	 对文件进行压缩和解压缩，压缩之后用“.gz”作为扩展名
>
> ​	还可以和tar命令一起构成Linux操作系统中比较流行的压缩文件格式
>
> ```python
> -d或--decompress或----uncompress：解开压缩文件；
> -f或——force：强行压缩文件。不理会文件名称或硬连接是否存在以及该文件是否为符号连接；
> -l或——list：列出压缩文件的相关信息；
> -L或——license：显示版本与版权信息；
> -n或--no-name：压缩文件时，不保存原来的文件名称及时间戳记；
> -N或——name：压缩文件时，保存原来的文件名称及时间戳记；
> -q或——quiet：不显示警告信息；
> -r或——recursive：递归处理，将指定目录下的所有文件及子目录一并处理；
> -t或——test：测试压缩文件是否正确无误；
> -v或——verbose：显示指令执行过程；
> -V或——version：显示版本信息；
> 
> 演示命令：
> angyang@yangyang-virtualmachine:~$ cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip *      #全部压缩
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip -dv *	#全部解压
> a1.txt.gz:	  8.3% -- replaced with a1.txt
> a2.txt.gz:	  9.1% -- replaced with a2.txt
> a.gz:	  2.4% -- replaced with a
> a.txt.gz:	  7.1% -- replaced with a.txt
> b.txt.gz:	  0.0% -- replaced with b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip *
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip -l *      #显示压缩后的信息
>          compressed        uncompressed  ratio uncompressed_name
>                  69                  48   8.3% a1.txt
>                  35                  11   9.1% a2.txt
>                  60                  41   2.4% a
>                  76                  56   7.1% a.txt
>                  26                   0   0.0% b.txt
>                 266                 156 -55.1% (totals)
> yangyang@yangyang-virtualmachine:~/Desktop$ touch text1.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip -r text1.txt 
> yangyang@yangyang-virtualmachine:~/Desktop$ mkdir check
> yangyang@yangyang-virtualmachine:~/Desktop$ cd check/
> yangyang@yangyang-virtualmachine:~/Desktop/check$ touch  a.txt
> yangyang@yangyang-virtualmachine:~/Desktop/check$ touch b.txt
> yangyang@yangyang-virtualmachine:~/Desktop/check$ touch c.txt
> yangyang@yangyang-virtualmachine:~/Desktop/check$ mkdir text
> yangyang@yangyang-virtualmachine:~/Desktop/check$ cd ..
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip -rv check    #递归压缩
> #注意：只是将目录下的文件全部递归压缩，对子目录不做操作
> check/a.txt:	  0.0% -- replaced with check/a.txt.gz
> check/b.txt:	  0.0% -- replaced with check/b.txt.gz
> check/c.txt:	  0.0% -- replaced with check/c.txt.gz
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip -dr check   #递归解压
> yangyang@yangyang-virtualmachine:~/Desktop$ cd check/
> yangyang@yangyang-virtualmachine:~/Desktop/check$ ls
> a.txt  b.txt  c.txt  text
> yangyang@yangyang-virtualmachine:~/Desktop/check$ cd ..
> yangyang@yangyang-virtualmachine:~/Desktop$ gzip -dv *
> a1.txt.gz:	  8.3% -- replaced with a1.txt
> a2.txt.gz:	  9.1% -- replaced with a2.txt
> a.gz:	  2.4% -- replaced with a
> a.txt.gz:	  7.1% -- replaced with a.txt
> b.txt.gz:	  0.0% -- replaced with b.txt
> gzip: check is a directory -- ignored
> text1.txt.gz:	  0.0% -- replaced with text1.txt
> ```

#### 2.vi和vim编辑器

> **vi命令**是UNIX操作系统最通用的全屏幕纯文本编辑器。Linux中的vi编辑器叫vim，它是vi的增强版（vi Improved），与vi编辑器完全兼容，而且实现了很多增强功能
>
> vim编辑器工作模式有三种：命令模式，输入模式【编辑模式】，末行模式
>
> 输入模式：可以完成文本文档的编辑操作
>
> 命令模式：可以完成对文本的操作命令
>
> 掌握：掌握三种工作模式之间的任意切换
>
> ```python
> 进入vi的命令 
>     vim filename :打开或新建文件，并将光标置于第一行首    ******
>     vi +n filename ：打开文件，并将光标置于第n行首 
>     vi + filename ：打开文件，并将光标置于最后一行首
>     vi filename1 filename2   :同时打开多个文件
>       
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ vim a1.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ vim +3 a1.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ vim + a1.txt
> 
> 插入文本类命令 
>   	i ：在光标前       ******
>   	I ：在当前行首 
>   	a：光标后        ******
>   	A：在当前行尾 
>   	o：在当前行之下新开一行        ******
>   	O：在当前行之上新开一行 
>   	r：替换当前字符 
>   	R：替换当前字符及其后的字符，直至按ESC键 
>   
> 移动光标 #在命令模式下使用
>   	j或下箭头 向下移动一行
>   	k或上箭头 向上移动一行
>   	h或左箭头 左移一个字符
>   	l或右箭头 右移一个字符
>   	w 　　　　右移一个词
>   	W 　　　　右移一个以空格分隔的词 
>   	b 　　　　左移一个词
>   	B 　　　　左移一个以空格分隔的词
>   	0 　　　　移到行首
>   	Ctrl-F　　向前翻页
>   	Ctrl-B　　向后翻页
>   	nG　　　　到第n行  ------》先按下数字，再按下G
>   	G 　　　　到最后一行
>   	gg	     第一行   -----》先按下g，再按下g
>   	n+       光标下移n行 
>   	n-       光标上移n行
>     
> esc:退出输入模式      ******
> 
> :set number：在命令模式下，用于在最左端显示行号；
> :set nonumber：在命令模式下，用于在最左端不显示行号；
> 
> 保存退出 
>   	:wq		执行存盘退出操作；      #对内容做修改之后使用，保存退出   *****
>     :wq!	#修改之后并且强制保存退出
> 	:w		执行存盘操作；
> 	:w！		执行强制存盘操作；
> 	:q		执行退出vi操作；
> 	:q！		执行强制退出vi操作；     #如果没有任何修改的时候使用  ******
> 	:e文件名	打开并编辑指定名称的文件；
> 	:n!		如果同时打开多个文件，则保存上个文件继续编辑下一个文件；
> 	:f		用于显示当前的文件名、光标所在行的行号以及显示比例；
> 	
> 删除操作【注意：和上面的插入文本类没有关系，进入vim后直接使用】 #在命令模式下使用
>   	x		删除光标处的单个字符 
>   	dd		删除光标所在行 
>   	dw		删除当前字符到单词尾（包括空格）的所有字符 
>   	de		删除当前字符到单词尾（不包括单词尾部的空格）的所有字符 
>   	d$		删除当前字符到行尾的所有字符 
>   	d^		删除当前字符到行首的所有字符 
>   	J		删除光标所在行行尾的换行符，相当于合并当前行和下一行的内容
>   	
> 替换操作
>   	:s/old/new 		将当前行中查找到的第一个字符“old” 串替换为“new”
>   	:#,#s/old/new 	在行号“#,#”范围内替换所有的字符串“old”为“new”
>   	:%s/old/new	    在整个文件范围内替换所有的字符串“old”为“new”
>   	:s/old/new/c 	在替换命令末尾加入c命令，将对每个替换动作提示用户进行确认
>   	
> 撤消操作 【注意：直接在输入模式下使用】
> 	u取消最近一次的操作，并恢复操作结果   *****
> 	#可以多次使用u命令恢复已进行的多步操作 
> 	U取消对当前行进行的所有操作 
> 	Ctrl + r对使用u命令撤销的操作进行恢复 
> ```

#### 3.用户管理

> 用户管理包括用户和组账号的管理
>
> 在Linux系统中，每个系统都必须有一个账号，并且对于不同的系统资源的使用权限
>
> root：超级管理员，通常用于系统的管理和维护，对Linux系统具有不受任何限制的操作权限

> ```
> linux使用文件保存用户信息 
> /etc/passwd 用户账户信息。
> /etc/shadow 安全用户账户信息。
> /etc/group 组账户信息。
> /etc/gshadow 安全组账户信息。
> /etc/default/useradd 账户创建的默认值。
> /etc/skel/ 包含默认文件的目录。
> /etc/login.defs Shadow 密码套件配置。
> ```

> 1>whoami     查看当前系统当前用户的用户名
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:/$ su root
> 密码： 
> root@yangyang-virtualmachine:/# whoami
> root
> ```

> 2>who     查看当前所有登录系统的用户信息
>
> ```python
> -q:只显示用户的登录账号的和登录用户的数量
> -u:显示列标题
> 
> 演示命令：
> root@yangyang-virtualmachine:/# su yangyang
> yangyang@yangyang-virtualmachine:/$ who
> yangyang tty7         2018-06-28 08:54 (:0)
> yangyang@yangyang-virtualmachine:/$ who -q
> yangyang
> # 用户数=1
> yangyang@yangyang-virtualmachine:/$ who -u
> yangyang tty7         2018-06-28 08:54 02:42        8992 (:0)
> ```

> 3>exit	退出
>
> 如果切换后的用户，则返回上一个登录的账号
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:/$ su root
> 密码： 
> root@yangyang-virtualmachine:/# exit
> exit
> yangyang@yangyang-virtualmachine:/$ su root
> 密码： 
> root@yangyang-virtualmachine:/# su yangyang
> yangyang@yangyang-virtualmachine:/$ su
> 密码： 
> root@yangyang-virtualmachine:/# exit
> exit
> yangyang@yangyang-virtualmachine:/$ su - 
> 密码： 
> root@yangyang-virtualmachine:~# exit
> 注销
> ```

> 4>su	切换用户
>
> 注意：如果不知名用户名，则默认切换到root用户
>
> 用法：
>
> ​	su  用户名
>
> ​	su  -   用户名
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:/$ su - root
> 密码： 
> root@yangyang-virtualmachine:~# su - yangyang
> yangyang@yangyang-virtualmachine:~$ pwd
> /home/yangyang
> yangyang@yangyang-virtualmachine:~$ 
> ```

> 5>useradd       添加用户
>
> 注意：添加普通用户，只能通过root添加
>
> ```python
> -c 备注 加上备注。并会将此备注文字加在/etc/passwd中的第5项字段中
> -d 用户主文件夹。指定用户登录所进入的目录，并赋予用户对该目录的的完全控制权        
> -e 有效期限。指定帐号的有效期限。格式为YYYY-MM-DD，将存储在/etc/shadow         
> -f 缓冲天数。限定密码过期后多少天，将该用户帐号停用       
> -g 主要组。设置用户所属的主要组  www.cit.cn           *******
> -G 次要组。设置用户所属的次要组，可设置多组         
> -M 强制不创建用户主文件夹         
> -m 强制建立用户主文件夹，并将/etc/skel/当中的文件复制到用户的根目录下      ****  
> -p 密码。输入该帐号的密码         
> -s shell。用户登录所使用的shell         
> -u uid。指定帐号的标志符user id，简称uid
> 
> 
> 演示命令：
> #第一种方式添加用户
> yangyang@yangyang-virtualmachine:~$ su root
> 密码： 
> root@yangyang-virtualmachine:/home/yangyang# useradd zhangsan    #添加用户
> root@yangyang-virtualmachine:/home/yangyang# su yangyang
> yangyang@yangyang-virtualmachine:~$ ls /home/
> yangyang         #本质没有添加进来
> yangyang@yangyang-virtualmachine:~$ su root
> 密码： 
> root@yangyang-virtualmachine:/home/yangyang# mkdir /home/zhangsan
>   #在home目录下创建一个和用户同名的目录
> root@yangyang-virtualmachine:/home/yangyang# exit
> exit
> yangyang@yangyang-virtualmachine:~$ ls /home/
> yangyang  zhangsan
> yangyang@yangyang-virtualmachine:~$ ls -l /home/
> 总用量 8
> drwxr-xr-x 31 yangyang rock 4096 6月  28 11:13 yangyang
> drwxr-xr-x  2 root     root 4096 6月  28 14:17 zhangsan
> yangyang@yangyang-virtualmachine:~$ sudo chown zhangsan:zhangsan /home/zhangsan				#将新建的用户和新建的用户目录联系起来
> [sudo] yangyang 的密码： 
> yangyang@yangyang-virtualmachine:~$ ls -l /home/
> 总用量 8
> drwxr-xr-x 31 yangyang rock     4096 6月  28 11:13 yangyang
> drwxr-xr-x  2 zhangsan zhangsan 4096 6月  28 14:17 zhangsan
> yangyang@yangyang-virtualmachine:~$ sudo passwd zhangsan
> 输入新的 UNIX 密码： 
> 重新输入新的 UNIX 密码： 
> passwd：已成功更新密码
> yangyang@yangyang-virtualmachine:~$ ls /home/
> yangyang  zhangsan
> yangyang@yangyang-virtualmachine:~$ su - zhangsan
> 密码： 
> $ ls
> $ su yangyang
> 密码： 
> yangyang@yangyang-virtualmachine:/home/zhangsan$ cd ../..
> yangyang@yangyang-virtualmachine:/$ ls -a /home/yangyang/.bash*  #查看配置文件
> /home/yangyang/.bash_history  /home/yangyang/.bashrc
> /home/yangyang/.bash_logout
> yangyang@yangyang-virtualmachine:/$ su - zhangsan
> 密码： 
> $ ls -a /etc/skel/       #查看配置文件
> .  ..  .bash_logout  .bashrc  examples.desktop	.profile
> $ cp /etc/skel/.bash* .     #将查到的文件拷贝到当前目录下
> $ ls -a
> .  ..  .bash_logout  .bashrc
> $ 注销        #按下ctrl+ d注销用户
> yangyang@yangyang-virtualmachine:/$ sudo vim /etc/passwd  #设置用户密码
> yangyang@yangyang-virtualmachine:/$ su - zhangsan
> 密码： 
> zhangsan@yangyang-virtualmachine:~$ su - yangyang
> 密码： 
> 
> #第二种方式添加用户
> yangyang@yangyang-virtualmachine:~$ sudo useradd -m -s /bin/bash lisi
> yangyang@yangyang-virtualmachine:~$ ls /home/
> lisi  yangyang  zhangsan
> yangyang@yangyang-virtualmachine:~$ sudo useradd -m xiaoli
> yangyang@yangyang-virtualmachine:~$ ls /home/
> lisi  xiaoli  yangyang  zhangsan
> yangyang@yangyang-virtualmachine:~$ su - zhangsan
> 密码： 
> 
> #第三种方式添加用户
> zhangsan@yangyang-virtualmachine:~$ sudo useradd -m hello
> [sudo] zhangsan 的密码： 
> zhangsan 不在 sudoers 文件中。此事将被报告。
> zhangsan@yangyang-virtualmachine:~$ su - root
> 密码： 
> root@yangyang-virtualmachine:~# vim /etc/sudoers
> root@yangyang-virtualmachine:~# 
> 
> 问题：按照第一种方式新增的用户和正常用户的使用有区别
> 正常用户：yangyang@yangyang-virtualmachine:~$ su - zhangsan
> 新增的用户：$ ls
> 
> 解决方案：需要手动添加配置文件，过程如下：
> yangyang@yangyang-virtualmachine:/$ su - zhangsan
> 密码： 
> $ ls -a /etc/skel/       #查看配置文件
> .  ..  .bash_logout  .bashrc  examples.desktop	.profile
> $ cp /etc/skel/.bash* .     #将查到的文件拷贝到当前目录下
> $ ls -a
> .  ..  .bash_logout  .bashrc
> $ 注销        #按下ctrl+ d注销用户
> yangyang@yangyang-virtualmachine:/$ sudo vim /etc/passwd  #设置用户密码
> yangyang@yangyang-virtualmachine:/$ su - zhangsan
> 密码： 
> zhangsan@yangyang-virtualmachine:~$
> ```

> 6>userdel        删除用户
>
> ```python
> userdel -r zhangsan   ：删除普通用户，同时自动删除用户所在的主目录
> userdel zhangsan：只是删除普通用户，不会自动删除用户所在的主目录，需要手动 rm -rf zhangsan
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ sudo userdel -r zhangsan
> [sudo] yangyang 的密码： 
> userdel: zhangsan 邮件池 (/var/mail/zhangsan) 未找到
> yangyang@yangyang-virtualmachine:~$ ls /home/
> yangyang
> ```

> 7>passwd    设置密码
>
> 注意：一般配合useradd命令使用，当添加一个新的普通用户时，一般会紧接着设置该用户的密码
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ sudo useradd -m abc   #添加用户
> yangyang@yangyang-virtualmachine:~$ sudo passwd abc
> 输入新的 UNIX 密码： 			#需要设置的密码
> 重新输入新的 UNIX 密码： 
> passwd：已成功更新密码
> yangyang@yangyang-virtualmachine:~$ su - abc
> 密码：        #新用户的密码
> abc@yangyang-virtualmachine:~$ 
> ```

> 8>查看用户组
>
> 用户组的作用：将多个用户管理在同一个组下，方便管理，可以让不同的用户享用同种权限
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$cat /etc/group
> ```

> 9>groupadd 			添加组
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ sudo useradd -m python -g python1805
> yangyang@yangyang-virtualmachine:~$ sudo passwd python
> 输入新的 UNIX 密码： 
> 重新输入新的 UNIX 密码： 
> passwd：已成功更新密码
> yangyang@yangyang-virtualmachine:~$ su - python
> 密码： 
> python@yangyang-virtualmachine:~$ ll
> 总用量 32
> drwxr-xr-x 2 python python1805 4096 6月  28 15:23 ./
> drwxr-xr-x 5 root   root       4096 6月  28 15:23 ../
> -rw-r--r-- 1 python python1805  220 9月   1  2015 .bash_logout
> -rw-r--r-- 1 python python1805 3771 9月   1  2015 .bashrc
> -rw-r--r-- 1 python python1805 8980 4月  20  2016 examples.desktop
> -rw-r--r-- 1 python python1805  655 6月  24  2016 .profile
> ```

> 10>usermod     	修改用户的基本信息
>
> ```python
> -c<备注> 　修改用户帐号的备注文字。 
> -d登入目录> 　修改用户登入时的目录。 
> -e<有效期限> 　修改帐号的有效期限。 
> -f<缓冲天数> 　修改在密码过期后多少天即关闭该帐号。 
> -g<群组> 　修改用户所属的群组。 
> -G<群组> 　修改用户所属的附加群组。 
> -l<帐号名称> 　修改用户帐号名称。 
> -L 　锁定用户密码，使密码无效。 
> -s<shell> 　修改用户登入后所使用的shell。 
> -u<uid> 　修改用户ID。 
> -U 　解除密码锁定。
> 
> 演示命令：
> angyang@yangyang-virtualmachine:~$ ls -l /home/
> 总用量 16
> drwxr-xr-x  2 abc      abc        4096 6月  28 14:59 abc
> drwxr-xr-x  2 jack     jack       4096 6月  28 15:30 jack
> drwxr-xr-x  2 python   python1805 4096 6月  28 15:23 python
> drwxr-xr-x 31 yangyang yangyang   4096 6月  28 14:36 yangyang
> yangyang@yangyang-virtualmachine:~$ sudo groupadd tom     #创建用户组
> yangyang@yangyang-virtualmachine:~$ sudo usermod -g jack tom   
> usermod：用户“tom”不存在				#修改用户的用户组
> yangyang@yangyang-virtualmachine:~$ sudo usermod -g tom jack
> yangyang@yangyang-virtualmachine:~$ ls -l /home/
> 总用量 16
> drwxr-xr-x  2 abc      abc        4096 6月  28 14:59 abc
> drwxr-xr-x  2 jack     tom        4096 6月  28 15:30 jack
> drwxr-xr-x  2 python   python1805 4096 6月  28 15:23 python
> drwxr-xr-x 31 yangyang yangyang   4096 6月  28 14:36 yangyang
> yangyang@yangyang-virtualmachine:~$ sudo usermod -l newuser jack #修改用户名
> yangyang@yangyang-virtualmachine:~$ ls -l /home/
> 总用量 16
> drwxr-xr-x  2 abc      abc        4096 6月  28 14:59 abc
> drwxr-xr-x  2 newuser  tom        4096 6月  28 15:30 jack
> drwxr-xr-x  2 python   python1805 4096 6月  28 15:23 python
> ```

> 11>groupdel 			删除组
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ sudo groupdel abc
> groupdel：不能移除用户“abc”的主组
> yangyang@yangyang-virtualmachine:~$ sudo groupdel python1805
> groupdel：不能移除用户“python”的主组
> yangyang@yangyang-virtualmachine:~$ sudo groupadd user11   
> yangyang@yangyang-virtualmachine:~$ sudo groupdel user11  #删除没有用户的组
> yangyang@yangyang-virtualmachine:~$ sudo userdel -r abc   #删除对于有用户组
> userdel: user abc is currently used by process 13160 
> yangyang@yangyang-virtualmachine:~$ 注销   #如果用户在使用中则使用ctrl+d注销
> yangyang@yangyang-virtualmachine:~$ sudo userdel -r abc   #注销之后再删除
> userdel: user abc is currently used by process 13160
> yangyang@yangyang-virtualmachine:~$ 注销
> abc@yangyang-virtualmachine:~$ 注销
> yangyang@yangyang-virtualmachine:~$ sudo userdel -r abc
> userdel: abc 邮件池 (/var/mail/abc) 未找到  
> ```

> 12>sudo      让当前用户暂时以管理员的身份root来执行命令

> 13>chmod     修改文件权限
>
> ```python
> drwxr-xr-x 31 yangyang yangyang   4096 6月  28 14:36 yangyang
> 
> #权限的意义
> rwx           			r-x  			 			r-x
> 当前用户的权限			  同组内其他用户的权限		   其他组内用户的权限
> r w x -
> 4 2 1 0
> 
> 演示命令：
> #字母法修改文件权限
> yangyang@yangyang-virtualmachine:~/Desktop$ ll
> 总用量 12
> drwxr-xr-x  2 yangyang yangyang 4096 6月  28 15:47 ./
> drwxr-xr-x 31 yangyang yangyang 4096 6月  28 15:47 ../
> -rw-r--r--  1 yangyang rock       20 6月  28 15:47 a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ chmod u+x a.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ll
> 总用量 12
> drwxr-xr-x  2 yangyang yangyang 4096 6月  28 15:47 ./
> drwxr-xr-x 31 yangyang yangyang 4096 6月  28 15:47 ../
> -rwxr--r--  1 yangyang rock       20 6月  28 15:47 a.txt*
>   
> #数字法修改文件权限
> yangyang@yangyang-virtualmachine:~/Desktop$ touch b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ll
> 总用量 12
> drwxr-xr-x  2 yangyang yangyang 4096 6月  28 15:52 ./
> drwxr-xr-x 31 yangyang yangyang 4096 6月  28 15:47 ../
> -rwxr--r--  1 yangyang rock       20 6月  28 15:47 a.txt*
> -rw-r--r--  1 yangyang rock        0 6月  28 15:52 b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ chmod 0764 b.txt
> yangyang@yangyang-virtualmachine:~/Desktop$ ll
> 总用量 12
> drwxr-xr-x  2 yangyang yangyang 4096 6月  28 15:52 ./
> drwxr-xr-x 31 yangyang yangyang 4096 6月  28 15:47 ../
> -rwxr--r--  1 yangyang rock       20 6月  28 15:47 a.txt*
> -rwxrw-r--  1 yangyang rock        0 6月  28 15:52 b.txt*
> ```

> 14>chown       修改文件所有者
>
> 格式：chown   新的用户  文件名

> 15>chgrp      修改文件所属组
>
> 格式：chgrp   新的用户  文件名

#### 4.系统管理

> 1>date   显示日期
>
> ```
> 日期格式化
> %Y     year
> %m     month (01..12)
> %d     day of month (e.g., 01)
> %H     hour (00..23)
> %I     hour (01..12)
> %M     minute (00..59)
> %S     second (00..60)
> 
> 演示命令：
> 
> ```

> 2>cal		显示一个日历
>
> ```
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ cal 
>       六月 2018         
> 日 一 二 三 四 五 六  
>                 1  2  
>  3  4  5  6  7  8  9  
> 10 11 12 13 14 15 16  
> 17 18 19 20 21 22 23  
> 24 25 26 27 28 29 30  
> ```

> 3>ps	报告当前系统的进程状态
>
> ```
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ ps -u
> USER        PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
> yangyang  13087  0.0  0.3  25248  6124 pts/4    Ss   14:56   0:00 bash
> yangyang  14078  0.0  0.1  39104  3284 pts/4    R+   16:42   0:00 ps -u
> ```
>
> 

> 4>kill	删除执行中的程序或工作
>
> ```
> -a：当处理当前进程时，不限制命令名和进程号的对应关系；
> -l <信息编号>：若不加<信息编号>选项，则-l参数会列出全部的信息名称；
> -p：指定kill 命令只打印相关进程的进程号，而不发送任何信号；
> -s <信息名称或编号>：指定要送出的信息；
> -u：指定用户
> 
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ kill -l
>  1) SIGHUP	 2) SIGINT	 3) SIGQUIT	 4) SIGILL	 5) SIGTRAP
>  6) SIGABRT	 7) SIGBUS	 8) SIGFPE	 9) SIGKILL	10) SIGUSR1
> 11) SIGSEGV	12) SIGUSR2	13) SIGPIPE	14) SIGALRM	15) SIGTERM
> 16) SIGSTKFLT	17) SIGCHLD	18) SIGCONT	19) SIGSTOP	20) SIGTSTP
> 21) SIGTTIN	22) SIGTTOU	23) SIGURG	24) SIGXCPU	25) SIGXFSZ
> 26) SIGVTALRM	27) SIGPROF	28) SIGWINCH	29) SIGIO	30) SIGPWR
> 31) SIGSYS	34) SIGRTMIN	35) SIGRTMIN+1	36) SIGRTMIN+2	37) SIGRTMIN+3
> 38) SIGRTMIN+4	39) SIGRTMIN+5	40) SIGRTMIN+6	41) SIGRTMIN+7	42) SIGRTMIN+8
> 43) SIGRTMIN+9	44) SIGRTMIN+10	45) SIGRTMIN+11	46) SIGRTMIN+12	47) SIGRTMIN+13
> 48) SIGRTMIN+14	49) SIGRTMIN+15	50) SIGRTMAX-14	51) SIGRTMAX-13	52) SIGRTMAX-12
> 53) SIGRTMAX-11	54) SIGRTMAX-10	55) SIGRTMAX-9	56) SIGRTMAX-8	57) SIGRTMAX-7
> 58) SIGRTMAX-6	59) SIGRTMAX-5	60) SIGRTMAX-4	61) SIGRTMAX-3	62) SIGRTMAX-2
> 63) SIGRTMAX-1	64) SIGRTMAX	
> ```

> 5>df      显示磁盘分区上的可使用的磁盘空间
>
> ​	注意：默认的单位为kb
>
> ```
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ df 
> df: /mnt/hgfs: 协议错误
> 文件系统          1K-块    已用    可用 已用% 挂载点
> udev             982640       0  982640    0% /dev
> tmpfs            201812    8928  192884    5% /run
> /dev/sda1      16381864 8263340 7263332   54% /
> tmpfs           1009040     280 1008760    1% /dev/shm
> tmpfs              5120       4    5116    1% /run/lock
> tmpfs           1009040       0 1009040    0% /sys/fs/cgroup
> tmpfs            201812      68  201744    1% /run/user/1000
> yangyang@yangyang-virtualmachine:~/Desktop$ df -h
> df: /mnt/hgfs: 协议错误
> 文件系统        容量  已用  可用 已用% 挂载点
> udev            960M     0  960M    0% /dev
> tmpfs           198M  8.8M  189M    5% /run
> /dev/sda1        16G  7.9G  7.0G   54% /
> tmpfs           986M  280K  986M    1% /dev/shm
> tmpfs           5.0M  4.0K  5.0M    1% /run/lock
> tmpfs           986M     0  986M    0% /sys/fs/cgroup
> tmpfs           198M   68K  198M    1% /run/user/1000
> ```

> 6>du  	显示文件的内存大小
>
> 注意：与df命令不同的是du命令是对文件和目录磁盘使用的空间的查看

> 7>free	显示当前系统未使用的和已使用的内存数目，还可以显示被内核使用的内存缓冲区
>
> ```
> 演示命令：
> free -m
>               total        used        free      shared  buff/cache   available
> Mem:           1970        1103         144          15         722         638
> Swap:          4093           5        4088
> 
> 
> 延时命令：
> total        used        free      shared  buff/cache   available
> Mem:           1970        1103         144          15         722         638
> Swap:          4093           5        4088
> 
> 全部		  已使用的      剩余的  共享的    缓存
> total = used + free
> 
> ```

> 8>其他
>
> ```
> reboot:重启
> shutdown -h now   :立即关机
> shutdown -r now   :立即重启
> shutdown -h +1    ：1分钟之后重启
> clear   :清屏，作用类似于ctrl+l
> 
> init 0: 关机
> init 6: 重启
> ```

> 9>ping   检测网络的连通性
>
> 10>ifconfig  查看网卡信息，ip地址等，相当于windows上的ipconfig
>
> ```
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop$ ifconfig
> ens33     Link encap:以太网  硬件地址 00:0c:29:8c:1e:35  
>           inet 地址:10.36.131.192  广播:10.36.131.255  掩码:255.255.255.0
>           inet6 地址: fe80::2025:7389:1aad:8cc8/64 Scope:Link
>           UP BROADCAST RUNNING MULTICAST  MTU:1500  跃点数:1
>           接收数据包:73625 错误:0 丢弃:0 过载:0 帧数:0
>           发送数据包:29011 错误:0 丢弃:0 过载:0 载波:0
>           碰撞:0 发送队列长度:1000 
>           接收字节:9001772 (9.0 MB)  发送字节:2018148 (2.0 MB)
> 
> lo        Link encap:本地环回  
>           inet 地址:127.0.0.1  掩码:255.0.0.0
>           inet6 地址: ::1/128 Scope:Host
>           UP LOOPBACK RUNNING  MTU:65536  跃点数:1
>           接收数据包:42021 错误:0 丢弃:0 过载:0 帧数:0
>           发送数据包:42021 错误:0 丢弃:0 过载:0 载波:0
>           碰撞:0 发送队列长度:1000 
>           接收字节:3381269 (3.3 MB)  发送字节:3381269 (3.3 MB)
> ```
>
> 

### 上堂回顾

> 1.文件管理：
>
> ​	sed:根据不同的条件提取文本行
>
> ​	tar:打包
>
> ​	gzip:压缩
>
> 2.vim编辑器
>
> ​	vim  filename
>
> ​	三种工作模式之间的切换：命令模式，输入模式，末行模式
>
> ​	流程：vim  filename-----》进入到命令模式-----》aios切换到输入模式-----》按下esc切换到命令模式------》：切换到末行模式------》按下回车切换到命令模式------》退出
>
> 3.用户管理
>
> ​	用户：
>
> ​		useradd
>
> ​		userdel 
>
> ​		usermod
>
> ​		passwd
>
> ​	用户组：
>
> ​		groupadd
>
> ​		groupdel
>
> ​	sudo    su       exit   
>
> 4.系统管理
>
> ​	ifconfig
>
> ​	ping

### 九、git的使用

#### 1.git简介

##### 1.1案例引入

> 如果你用Word写过毕业论文，那你一定有这样的经历：
>
> 想删除一个段落，又怕将来想恢复找不回来怎么办？有办法，先把当前文件“另存为……”一个新的Word文件，再接着改，改到一定程度，再“另存为……”一个新文件，这样一直改下去，最后你的Word文档变成了这样：
>
> ![lots-of-docs](https://cdn.liaoxuefeng.com/cdn/files/attachments/0013848606651673ff1c83932d249118bf8fd5c58c15ca2000/0)
>
> 过了一周，你想找回被删除的文字，但是已经记不清删除前保存在哪个文件里了，只好一个一个文件去找，真麻烦。
>
> 看着一堆乱七八糟的文件，想保留最新的一个，然后把其他的删掉，又怕哪天会用上，还不敢删，真郁闷。
>
> 更要命的是，有些部分需要你的财务同事帮助填写，于是你把文件Copy到U盘里给她（也可能通过Email发送一份给她），然后，你继续修改Word文件。一天后，同事再把Word文件传给你，此时，你必须想想，发给她之后到你收到她的文件期间，你作了哪些改动，得把你的改动和她的部分合并，真困难。
>
> 于是你想，如果有一个软件，不但能自动帮我记录每次文件的改动，还可以让同事协作编辑，这样就不用自己管理一堆类似的文件了，也不需要把文件传来传去。如果想查看某次改动，只需要在软件里瞄一眼就可以，岂不是很方便？
>
> 这个软件用起来就应该像这个样子，能记录每次文件的改动：
>
> | 版本 | 文件名      | 用户 | 说明                   | 日期       |
> | ---- | ----------- | ---- | ---------------------- | ---------- |
> | 1    | service.doc | 张三 | 删除了软件服务条款5    | 7/12 10:38 |
> | 2    | service.doc | 张三 | 增加了License人数限制  | 7/12 18:09 |
> | 3    | service.doc | 李四 | 财务部门调整了合同金额 | 7/13 9:51  |
> | 4    | service.doc | 张三 | 延长了免费升级周期     | 7/14 15:17 |
>
> 这样，你就结束了手动管理多个“版本”的史前时代，进入到版本控制的20世纪。
>
> Git是目前世界上最先进的分布式版本控制系统（没有之一）。
>
> Git有什么特点？简单来说就是：高端大气上档次！

##### 1.2git的由来

> ​	很多人都知道，Linus在1991年创建了开源的Linux，从此，Linux系统不断发展，已经成为最大的服务器系统软件了。
>
> ​	Linus虽然创建了Linux，但Linux的壮大是靠全世界热心的志愿者参与的，这么多人在世界各地为Linux编写代码，那Linux的代码是如何管理的呢？
>
> ​	事实是，在2002年以前，世界各地的志愿者把源代码文件通过diff的方式发给Linus，然后由Linus本人通过手工方式合并代码！
>
> ​	你也许会想，为什么Linus不把Linux代码放到版本控制系统里呢？不是有CVS、SVN这些免费的版本控制系统吗？因为Linus坚定地反对CVS和SVN，这些集中式的版本控制系统不但速度慢，而且必须联网才能使用。有一些商用的版本控制系统，虽然比CVS、SVN好用，但那是付费的，和Linux的开源精神不符。
>
> ​	不过，到了2002年，Linux系统已经发展了十年了，代码库之大让Linus很难继续通过手工方式管理了，社区的弟兄们也对这种方式表达了强烈不满，于是Linus选择了一个商业的版本控制系统BitKeeper，BitKeeper的东家BitMover公司出于人道主义精神，授权Linux社区免费使用这个版本控制系统。
>
> ​	安定团结的大好局面在2005年就被打破了，原因是Linux社区牛人聚集，不免沾染了一些梁山好汉的江湖习气。开发Samba的Andrew试图破解BitKeeper的协议（这么干的其实也不只他一个），被BitMover公司发现了（监控工作做得不错！），于是BitMover公司怒了，要收回Linux社区的免费使用权。
>
> ​	Linus可以向BitMover公司道个歉，保证以后严格管教弟兄们，嗯，这是不可能的。实际情况是这样的：
>
> ​	Linus花了两周时间自己用C写了一个分布式版本控制系统，这就是Git！一个月之内，Linux系统的源码已经由Git管理了！牛是怎么定义的呢？大家可以体会一下。
>
> ​	Git迅速成为最流行的分布式版本控制系统，尤其是2008年，GitHub网站上线了，它为开源项目免费提供Git存储，无数开源项目开始迁移至GitHub，包括jQuery，PHP，Ruby等等。
>
> 历史就是这么偶然，如果不是当年BitMover公司威胁Linux社区，可能现在我们就没有免费而超级好用的Git了

##### 1.3集中式和分布式

> ​	SVN都是集中式的版本控制系统，而Git是分布式版本控制系统，集中式和分布式版本控制系统有什么区别呢？
>
> ​	集中式版本控制系统：版本库是集中存放在中央服务器的，而干活的时候，用的都是自己的电脑，所以要先从中央服务器取得最新的版本，然后开始干活，干完活了，再把自己的活推送给中央服务器。例如：中央服务器就好比是一个图书馆，你要改一本书，必须先从图书馆借出来，然后回到家自己改，改完了，再放回图书馆【缺点：必须联网才能工作，如果在局域网内还好，带宽够大，速度够快，可如果在互联网上，遇到网速慢的话，可能提交一个10M的文件就需要5分钟，这还不得把人给憋死啊】
>
> ​	分布式版本控制系统：根本没有“中央服务器”，每个人的电脑上都是一个完整的版本库，这样，你工作的时候，就不需要联网了，因为版本库就在你自己的电脑上。如果是一个团队合作工作，比方说你在自己电脑上改了文件A，你的同事也在他的电脑上改了文件A，这时，你们俩之间只需把各自的修改推送给对方，就可以互相看到对方的修改了
>
> ​	二者之间的区别：和集中式版本控制系统相比，分布式版本控制系统的安全性要高很多，因为每个人电脑里都有完整的版本库，某一个人的电脑坏掉了不要紧，随便从其他人那里复制一个就可以了。而集中式版本控制系统的中央服务器要是出了问题，所有人都没法干活了。	
>
> ​	实际情况：使用分布式版本控制系统的时候，其实很少在两人之间的电脑上推送版本库的修改，因为可能你们俩不在一个局域网内，两台电脑互相访问不了，也可能今天你的同事病了，他的电脑压根没有开机。因此，分布式版本控制系统通常也有一台充当“中央服务器”的电脑，但这个服务器的作用仅仅是用来方便“交换”大家的修改，没有它大家也一样干活，只是交换修改不方便而已。
>
> ​	当然，Git的优势不单是不必联网这么简单，后面我们还会看到Git极其强大的分支管理，把SVN等远远抛在了后面。

#### 2.安装git

> git：查看是否已经安装
>
> sudo apt-get install git  ：安装

#### 3.创建版本库

##### 3.1什么是版本库

> 版本库又被称为仓库，【repository】,初期可以理解为一个目录，这个目录里面管理的文件都可以被称为被git管理起来的，每个文件的修改，删除等的操作git都能进行跟踪

##### 3.2创建版本库

> git init：将一个普通目录变成版本库
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ cd Desktop/
> yangyang@yangyang-virtualmachine:~/Desktop$ mkdir python1805
> yangyang@yangyang-virtualmachine:~/Desktop$ cd python1805/
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ pwd
> /home/yangyang/Desktop/python1805
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git init
> 已初始化空的 Git 仓库于 /home/yangyang/Desktop/python1805/.git/
> #就创建一个git仓库【版本库】，
> 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ ls
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ ls -a
> .  ..  .git
> #.git是一个目录，就是用来跟踪管理版本库
> 
> #注意：也不一定目录是空的，但是为了安全起见，最好以一个空的目录作为版本库
> ```

##### 3.3把文件添加到版本库

> 注意：所有的版本控制系统都是跟踪的是文件的改动
>
> git add  filename :将文件添加到缓存区
>
> git commit -m "日志" ：提交文件到版本库【仓库】
>
> ```python
> 演示命令：
> angyang@yangyang-virtualmachine:~/Desktop/python1805$ touch text.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "create a new file and init"
> 
> *** 请告诉我你是谁。		#不知道主人是谁，则需要配置用户名和邮箱
> 						 #注意：用户名和邮箱来自github上的注册
> 
> 运行
> 
>   git config --global user.email "you@example.com"
>   git config --global user.name "Your Name"
> 
> 来设置您账号的缺省身份标识。
> 如果仅在本仓库设置身份标识，则省略 --global 参数。
> fatal: 无法自动探测邮件地址（得到 'yangyang@yangyang-virtualmachine.(none)'）
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git config --global user.email "18501970795@163.com"		#配置github上的邮箱
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git config --global user.name "yangyang-git"				#配置github上的用户名
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "create a new file and init"	
> #-m后面输入的是本次提交的说明【就是所谓的日志】，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录
> [master（根提交） d4b0bde] create a new file and init
>  1 file changed, 1 insertion(+)
>  create mode 100644 text.txt
> #git commit命令执行成功后会告诉你，1 file changed：1个文件被改动（我们新添加的readme.txt文件）；3 insertions：插入了一行内容
> 
> #再次修改文件，则重复git add和git commit命令
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "add hello" 
> [master 1f12c8b] add hello
>  1 file changed, 1 insertion(+)
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ 
> ```
>
> 问题：为什么Git添加文件需要add，commit一共两步呢？因为commit可以一次提交很多文件，所以你可以多次add不同的文件，如下：
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ touch text1.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ touch text2.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text1.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text2.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "create twofiles"
> [master ce63cb0] create twofiles
>  2 files changed, 0 insertions(+), 0 deletions(-)
>  create mode 100644 text1.txt
>  create mode 100644 text2.txt
>   
>   #总结：add一次添加一个文件，commit可以一次提交多个文件
> ```

#### 4.时光穿梭机【覆水可收】

> git status:查看仓库当前的状态
>
> git diff  filename:查看仓库具体的改动
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	修改：     text.txt
> 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "add 111"
> [master 3af9e8e] add 111
>  1 file changed, 1 insertion(+)
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 无文件要提交，干净的工作区
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git diff text.txt
> diff --git a/text.txt b/text.txt
> index 4892bab..cbb039d 100644
> --- a/text.txt
> +++ b/text.txt
> @@ -1,3 +1,3 @@
>  this is a text
>  hello
> -1111
> +11112222
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "222"
> [master 55804ad] 222
>  1 file changed, 1 insertion(+), 1 deletion(-)
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git diff text.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ 
> ```

##### 4.1版本回退

> 工作原理：每当修改一个文件，并且使用commit提交之后，其实就相当于保存了一个快照
>
> 需求：回退到上一个版本
>
> 补充：要回退版本，首先需要知道当前处于哪个版本，在git中，用HEAD表示当前版本，上一个版本是HEAD^,上上个版本是HEAD^^,如果向上找100个版本，则表示为HEAD~100
>
> git  reset  --hard  版本号【commit id】
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git log
> commit 55804ad1c9bca1d98d366e28e50ecbfac2c82597 (HEAD -> master)
> Author: yangyang-git <18501970795@163.com>
> Date:   Fri Jun 29 10:31:55 2018 +0800
> 
>     222
> 
> commit 3af9e8eeb2d9d5dfb04e52968c255d0dd5e3e8ee
> Author: yangyang-git <18501970795@163.com>
> Date:   Fri Jun 29 10:28:47 2018 +0800
> 
>     add 111
> 
> commit ce63cb0594622577d144372d8c48dcabee631973
> Author: yangyang-git <18501970795@163.com>
> Date:   Fri Jun 29 10:05:22 2018 +0800
> 
>     create twofiles
> 
> commit 1f12c8b33abea0c7c0ae195aaa7ef18894681137
> Author: yangyang-git <18501970795@163.com>
> Date:   Fri Jun 29 10:03:26 2018 +0800
> 
>     add hello
> 
> commit d4b0bde029497a68dcacb026fd299b90c0604116
> Author: yangyang-git <18501970795@163.com>
> Date:   Fri Jun 29 10:00:33 2018 +0800
> 
>     create a new file and init
> 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git log --pretty=oneline
> 55804ad1c9bca1d98d366e28e50ecbfac2c82597 (HEAD -> master) 222
> 3af9e8eeb2d9d5dfb04e52968c255d0dd5e3e8ee add 111
> ce63cb0594622577d144372d8c48dcabee631973 create twofiles
> 1f12c8b33abea0c7c0ae195aaa7ef18894681137 add hello
> d4b0bde029497a68dcacb026fd299b90c0604116 create a new file and init
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reset --hard HEAD^
> HEAD 现在位于 3af9e8e add 111
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cat text.txt 
> this is a text
> hello
> 1111
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git log --pretty=oneline
> 3af9e8eeb2d9d5dfb04e52968c255d0dd5e3e8ee (HEAD -> master) add 111
> ce63cb0594622577d144372d8c48dcabee631973 create twofiles
> 1f12c8b33abea0c7c0ae195aaa7ef18894681137 add hello
> d4b0bde029497a68dcacb026fd299b90c0604116 create a new file and init
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reset --hard 55804ad1
> HEAD 现在位于 55804ad 222
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cat text.txt 
> this is a text
> hello
> 11112222
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reset --hard HEAD^
> HEAD 现在位于 3af9e8e add 111
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reflog
> 3af9e8e (HEAD -> master) HEAD@{0}: reset: moving to HEAD^
> 55804ad HEAD@{1}: reset: moving to 55804ad1
> 3af9e8e (HEAD -> master) HEAD@{2}: reset: moving to HEAD^
> 55804ad HEAD@{3}: commit: 222
> 3af9e8e (HEAD -> master) HEAD@{4}: commit: add 111
> ce63cb0 HEAD@{5}: commit: create twofiles
> 1f12c8b HEAD@{6}: commit: add hello
> d4b0bde HEAD@{7}: commit (initial): create a new file and init
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reset --hard 55804ad
> HEAD 现在位于 55804ad 222
> ```
>
> 总结：
>
> - HEAD指向的是当前版本，所以，git在历史的版本之间来回切换，使用git reset --hard commit id
> - 切换版本前，可以使用git log查看提交历史记录，以便于确定回到哪个历史版本
> - 要重返未来，用git reflog查看历史执行过的git操作，从上往下寻找第一个commit的操作，则是未来的最新的版本

##### 4.2工作区和暂存区

> 工作区：working Driectory，就是你电脑中的能看到的目录【python1805】
>
> 版本库：工作区中有一个隐藏的目录.git,该目录就是git中的版本库
>
> ​	版本库中存放了很多的数据，其中包括暂存区【缓存区，stage或者index】，还有git为我们自动创建的第一个分支master【主分支】，以及指向master的一个指针HEAD
>
> 往git版本库中添加文件，分为两步：
>
> ​	a.git add,实际是将文件添加到暂存区中
>
> ​	b.git commit  .实际是将暂存区的文件提交到当前分支【主分支】
>
> ```python
> 演示命令：
> #a.修改text.txt文件
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> #b.在工作区中新增一个check.txt文本文件
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ touch check.txt
> #c.在check.txt文件中新增内容
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim check.txt
> #d.使用git status查看一下当前的状态
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 尚未暂存以备提交的变更：
>   （使用 "git add <文件>..." 更新要提交的内容）
>   （使用 "git checkout -- <文件>..." 丢弃工作区的改动）
> 
> 	修改：     text.txt
> 
> 未跟踪的文件:
>   （使用 "git add <文件>..." 以包含要提交的内容）
> 
> 	check.txt
> 
> 修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
> #Git非常清楚地告诉我们，text.txt被修改了，而check.txt还从来没有被添加过，所以它的状态是未跟踪
> 
> #e.将两个文件都添加到暂存区
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add check.txt 
> #f.再次查看
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	新文件：   check.txt
> 	修改：     text.txt
> #g.将两个文件提交到分支
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "modify textxt and create a new file named check"
> [master 9885393] modify textxt and create a new file named check
>  2 files changed, 2 insertions(+)
>  create mode 100644 check.txt
> #h.再次查看
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 无文件要提交，干净的工作区
> yangyang@yangyang-virtual
> 
> #一旦提交后，如果你又没有对工作区做任何修改，那么工作区就是干净的
> ```

##### 4.3管理修改

> 注意：git跟踪管理的是修改，并非文件
>
> ```python
> 演示命令：
> 3af9e8e (HEAD -> master) HEAD@{2}: reset: moving to HEAD^
> 55804ad HEAD@{3}: commit: 222
> 3af9e8e (HEAD -> master) HEAD@{4}: commit: add 111
> ce63cb0 HEAD@{5}: commit: create twofiles
> 1f12c8b HEAD@{6}: commit: add hello
> d4b0bde HEAD@{7}: commit (initial): create a new file and init
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reset --hard 55804ad
> HEAD 现在位于 55804ad 222
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ touch check.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim check.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 尚未暂存以备提交的变更：
>   （使用 "git add <文件>..." 更新要提交的内容）
>   （使用 "git checkout -- <文件>..." 丢弃工作区的改动）
> 
> 	修改：     text.txt
> 
> 未跟踪的文件:
>   （使用 "git add <文件>..." 以包含要提交的内容）
> 
> 	check.txt
> 
> 修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add check.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	新文件：   check.txt
> 	修改：     text.txt
> 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "modify textxt and create a new file named check"
> [master 9885393] modify textxt and create a new file named check
>  2 files changed, 2 insertions(+)
>  create mode 100644 check.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 无文件要提交，干净的工作区
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cat text.txt 
> this is a text
> hello
> 11112222
> 3333
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	修改：     text.txt
> 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "add 44 & 55"
> [master ad2c692] add 44 & 55
>  1 file changed, 1 insertion(+)
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 尚未暂存以备提交的变更：
>   （使用 "git add <文件>..." 更新要提交的内容）
>   （使用 "git checkout -- <文件>..." 丢弃工作区的改动）
> 
> 	修改：     text.txt
> 
> 修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git diff HEAD -- text.txt
> diff --git a/text.txt b/text.txt    
> index e1fd18b..4ae8e5f 100644
> --- a/text.txt
> +++ b/text.txt
> @@ -3,3 +3,4 @@ hello
>  11112222
>  3333
>  44444
> +55555
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "add 55"
> [master e233f10] add 55
>  1 file changed, 1 insertion(+)
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git diff HEAD -- text.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ 
> ```

##### 4.4撤销修改

> a.修改了文件内容，但是还没有添加到暂存区
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 尚未暂存以备提交的变更：
>   （使用 "git add <文件>..." 更新要提交的内容）
>   （使用 "git checkout -- <文件>..." 丢弃工作区的改动）
> 
> 	修改：     text.txt
> 
> 修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cat text.txt 
> this is a text
> hello
> 11112222
> 3333
> 44444
> 55555
> stupid boss
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git checkout -- text.txt					#回到最近一次git commit或git add时的状态
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cat text.txt
> this is a text
> hello
> 11112222
> 3333
> 44444
> 55555
> ```
>
> b.不但修改了内容，还添加到了暂存区，但是还没有提交
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	修改：     text.txt
> 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reset HEAD text.txt
> 重置后取消暂存的变更：        #把暂存区的修改撤销掉
> M	text.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 尚未暂存以备提交的变更：
>   （使用 "git add <文件>..." 更新要提交的内容）
>   （使用 "git checkout -- <文件>..." 丢弃工作区的改动）
> 
> 	修改：     text.txt
> 
> 修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git checkout -- text.txt     #丢弃工作区的修改
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 无文件要提交，干净的工作区
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cat text.txt 
> this is a text
> hello
> 11112222
> 3333
> 44444
> 55555
> ```
>
> c.直接将修改的内容提交到了版本库
>
>    实质：版本回退
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ vim text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add text.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "fehj"
> [master 8ac0ac4] fehj
>  1 file changed, 1 insertion(+)
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git reset --hard HEAD^
> HEAD 现在位于 e233f10 add 55
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cat text.txt 
> this is a text
> hello
> 11112222
> 3333
> 44444
> 55555
> ```

##### 4.5删除文件

> 在git中，删除文件也是一个修改操作
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ touch newfile.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git add newfile.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "create new file"
> [master f86d2bd] create new file
>  1 file changed, 0 insertions(+), 0 deletions(-)
>  create mode 100644 newfile.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ rm newfile.txt 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git tsatus
> git：'tsatus' 不是一个 git 命令。参见 'git --help'。
> 
> 最相似的命令是
> 	status
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 尚未暂存以备提交的变更：
>   （使用 "git add/rm <文件>..." 更新要提交的内容）
>   （使用 "git checkout -- <文件>..." 丢弃工作区的改动）
> 
> 	删除：     newfile.txt
> 
> 修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git rm newfile.txt 
> rm 'newfile.txt'
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	删除：     newfile.txt
> 
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git commit -m "delete newfile"
> [master d41fc15] delete newfile
>  1 file changed, 0 insertions(+), 0 deletions(-)
>  delete mode 100644 newfile.txt
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ git status
> 位于分支 master
> 无文件要提交，干净的工作区
> ```

#### 5.远程仓库

##### 5.1建立远程仓库的准备工作

> 步骤：
>
> a.创建github账号
>
> b.生成ssh key【秘钥，建立本地和网络之间的连接】
>
> ​	命令：ssh-keygen  -t   rsa  -C    "github的注册邮箱"
>
> c.添加到github
>
> d.检测是否添加成功
>
> ​	命令:ssh  -T   git@github.com
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ ssh-keygen  -t   rsa  -C    "18501970795@163.com"      #生成ssh key
> Generating public/private rsa key pair.
> Enter file in which to save the key (/home/yangyang/.ssh/id_rsa): 
> Created directory '/home/yangyang/.ssh'.
> Enter passphrase (empty for no passphrase): 
> Enter same passphrase again: 
> Your identification has been saved in /home/yangyang/.ssh/id_rsa.
> Your public key has been saved in /home/yangyang/.ssh/id_rsa.pub.
> The key fingerprint is:
> SHA256:o/KqM3kWKnQBZL8xGGyxhO6n82YJpN6YQfTcZMbp/3E 18501970795@163.com
> The key's randomart image is:
> +---[RSA 2048]----+
> |+*. . .          |
> |+==  *           |
> |+o++*            |
> | + ++o           |
> |=  .. . S        |
> |.= o.  o o E     |
> |o Xoo.. . o      |
> |.*==oo   .       |
> | .*B...          |
> +----[SHA256]-----+
> yangyang@yangyang-virtualmachine:~/Desktop/python1805$ cd ../..
> yangyang@yangyang-virtualmachine:~$ cd .ssh/
> yangyang@yangyang-virtualmachine:~/.ssh$ ls
> id_rsa  id_rsa.pub
> yangyang@yangyang-virtualmachine:~/.ssh$ cat id_rsa.pub      #查看生成的公钥
> ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCwiwfMpduAI7BP7ItaoZ8iyqWwN4io6ErpF9wNWLHXHrKSgR5A/tcVW5T90/q7v/HDgMQ8uBcF+WLBKamYVG31mj43yu2io/FRmEoSHKbRW0Q5aBtlu9bnvUsiJVI4F8eI9O9/b1iiAaQBta5swEkUUqJ6e2ZpKxeye5HU5Hgm36zEjT4EIflMr4ox/+WQmVYLf9lA7IMvYpmRd3cqtoGoxCdcmUu3T/hi9anYhlrsUxda46w+XC2ckZ1K0ZE3lrQOs0HQX9f4HQrKZupar8+GYst3dBQZz+V1YP7QmfMlSB0sM2s32SurSSO4ae2A3Oho8TPvuhJLp6Oufr+McK4j 18501970795@163.com
> ```

##### 5.2.将本地仓库和远程仓库联系起来

> 演示命令：
>
> ```python
> chenxushu@chenxushu:~$ cd Desktop/
> chenxushu@chenxushu:~/Desktop$ cd python1805/
> chenxushu@chenxushu:~/Desktop/python1805$ git remote add origin1 git@github.com:chenxushu1025/python1805.git   #建立连接
> chenxushu@chenxushu:~/Desktop/python1805$ git push -u origin1 master
> 对象计数中: 22, 完成.		#推送master分支并与远程master产生关联
> Delta compression using up to 2 threads.
> 压缩对象中: 100% (13/13), 完成.
> 写入对象中: 100% (22/22), 1.79 KiB | 918.00 KiB/s, 完成.
> Total 22 (delta 2), reused 0 (delta 0)
> remote: Resolving deltas: 100% (2/2), done.
> To github.com:chenxushu1025/python1805.git
>  * [new branch]      master -> master
> 分支 'master' 设置为跟踪来自 'origin1' 的远程分支 'master'。
> chenxushu@chenxushu:~/Desktop/python1805$ ls
> text1.txt  text2.txt  text.txt
> chenxushu@chenxushu:~/Desktop/python1805$ vim text1.txt 
> chenxushu@chenxushu:~/Desktop/python1805$ git add text1.txt 
> chenxushu@chenxushu:~/Desktop/python1805$ git commit -m "modify text1.txt"
> [master 69f0343] modify text1.txt
>  1 file changed, 1 insertion(+)
> chenxushu@chenxushu:~/Desktop/python1805$ git push origin1 master
> 对象计数中: 3, 完成.
> Delta compression using up to 2 threads.
> 压缩对象中: 100% (2/2), 完成.
> 写入对象中: 100% (3/3), 308 bytes | 308.00 KiB/s, 完成.
> Total 3 (delta 0), reused 0 (delta 0)
> To github.com:chenxushu1025/python180
> ```
>
> 总结：
>
> - 要关联一个远程仓库，使用命令 git remote add origin git@github.com:username/repoName.git
> - 关联成功之后 ，使用命令git push -u  origin master第一次推送master分支的内容到远程仓库
> - 以后，每次本地提交之后，只需要使用命令git  push   origin master推送最新的修改【本地修改----》add到暂存区---》commit到本地仓库----》push到远程仓库】

5.3从远程仓库克隆

> git clone git@github.com:username/repoName.git
>
> ```python
> 演示命令：
> chenxushu@chenxushu:~/Desktop/python1805$ cd ..
> chenxushu@chenxushu:~/Desktop$ git clone git@github.com:chenxushu1025/clonegithub.git   #从远程仓库克隆
> 正克隆到 'clonegithub'...
> remote: Counting objects: 3, done.
> remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
> 接收对象中: 100% (3/3), 完成.
> chenxushu@chenxushu:~/Desktop$ cd clonegithub/
> chenxushu@chenxushu:~/Desktop/clonegithub$ ls
> README.md
> chenxushu@chenxushu:~/Desktop/clonegithub$ vim README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git add README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git commit -m "modefy"[master 4d3b04a] modefy
>  1 file changed, 2 insertions(+), 1 deletion(-)
> chenxushu@chenxushu:~/Desktop/clonegithub$ git push origin master
> Warning: Permanently added the RSA host key for IP address '52.74.223.119' to the list of known hosts.
> 对象计数中: 3, 完成.
> 写入对象中: 100% (3/3), 258 bytes | 258.00 KiB/s, 完成.
> Total 3 (delta 0), reused 0 (delta 0)
> To github.com:chenxushu1025/clonegithub.git
>    24ee8e4..4d3b04a  master -> master
>     
> #克隆到本地之后，就可以任意修改本地工作区中的文件，修改完成之后，首先将修改add到暂存区，然后将暂存区中的修改提交到本地仓库，最后将本地仓库中的修改推送到远程仓库
> ```

#### 6.分支管理

##### 6.1.创建和合并分支

> ```python
> 演示命令：
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout -b dev
> 切换到一个新分支 'dev'
> chenxushu@chenxushu:~/Desktop/clonegithub$ git branch
> * dev
>   master
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout master
> 切换到分支 'master'
> 您的分支与上游分支 'origin/master' 一致。
> chenxushu@chenxushu:~/Desktop/clonegithub$ git branch
>   dev
> * master
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout dev
> 切换到分支 'dev'
> chenxushu@chenxushu:~/Desktop/clonegithub$ vim README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git add README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git commit -m "111"
> [dev 122ae1f] 111
>  1 file changed, 1 insertion(+)
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout master
> 切换到分支 'master'
> 您的分支与上游分支 'origin/master' 一致。
> chenxushu@chenxushu:~/Desktop/clonegithub$ cat README.md 
> # clonegithub
> hello
> chenxushu@chenxushu:~/Desktop/clonegithub$ git merge dev
> 更新 4d3b04a..122ae1f
> Fast-forward
>  README.md | 1 +
>  1 file changed, 1 insertion(+)
> chenxushu@chenxushu:~/Desktop/clonegithub$ cat README.md 
> # clonegithub
> hello
> 1111
> chenxushu@chenxushu:~/Desktop/clonegithub$ git branch -d dev
> 已删除分支 dev（曾为 122ae1f）。
> ```
>
> 总结：
>
> - git鼓励大量使用分支
> - 查看分支：git branch
> - 创建分支：git checkout -b  name  【-b创建分支并且同时切换到子分支下】
> - 切换分支：git checkout name
> - 合并某个子分支到当前分支：git  merge name
> - 删除分支：git branch -d name

##### 6.2解决冲突

> ```python
> 演示命令：
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout -b feature1
> 切换到一个新分支 'feature1'
> chenxushu@chenxushu:~/Desktop/clonegithub$ vim README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git add README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git commit -m "add hello and hi"
> [feature1 0296b41] add hello and hi
>  1 file changed, 1 insertion(+)
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout master
> 切换到分支 'master'
> 您的分支领先 'origin/master' 共 1 个提交。
>   （使用 "git push" 来发布您的本地提交）
> chenxushu@chenxushu:~/Desktop/clonegithub$ vim README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git add Re
> fatal: 路径规格 'Re' 未匹配任何文件
> chenxushu@chenxushu:~/Desktop/clonegithub$ git add README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git commit -m "add hello & hi"
> [master 594d625] add hello & hi
>  1 file changed, 1 insertion(+)
> chenxushu@chenxushu:~/Desktop/clonegithub$ git merge feature1
> 自动合并 README.md
> 冲突（内容）：合并冲突于 README.md
> 自动合并失败，修正冲突然后提交修正的结果。
> chenxushu@chenxushu:~/Desktop/clonegithub$ git status
> 位于分支 master
> 您的分支领先 'origin/master' 共 2 个提交。
>   （使用 "git push" 来发布您的本地提交）
> 
> 您有尚未合并的路径。
>   （解决冲突并运行 "git commit"）
>   （使用 "git merge --abort" 终止合并）
> 
> 未合并的路径：
>   （使用 "git add <文件>..." 标记解决方案）
> 
> 	双方修改：   README.md
> 
> 修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
> chenxushu@chenxushu:~/Desktop/clonegithub$ vim README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git add README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git commit -m "fix conflict"
> [master 5b37524] fix conflict
> chenxushu@chenxushu:~/Desktop/clonegithub$ git log  --graph#合并后，我们用git log看看分支历史
> ```

> 总结：
>
> - 当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。
> - 解决冲突就是把Git合并失败的文件手动编辑为我们希望的内容，再提交。
> - 用git log --graph命令可以看到分支合并图

##### 6.3分支合并策略

> ​	合并分支时，如果可能，Git会用Fast forward模式，但这种模式下，删除分支后，会丢掉分支信息
>
> ​	如果要强制禁用Fast forward模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信息

> ```python
> 演示命令：
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout -b dev
> 切换到一个新分支 'dev'
> chenxushu@chenxushu:~/Desktop/clonegithub$ vim README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git add README.md 
> chenxushu@chenxushu:~/Desktop/clonegithub$ git commit -m "222"
> [dev 8337c54] 222
>  1 file changed, 1 insertion(+)
> chenxushu@chenxushu:~/Desktop/clonegithub$ git checkout master
> 切换到分支 'master'
> 您的分支领先 'origin/master' 共 4 个提交。
>   （使用 "git push" 来发布您的本地提交）
> chenxushu@chenxushu:~/Desktop/clonegithub$ git merge --no-ff -m "222-1" dev
> #准备合并dev分支，请注意--no-ff参数，表示禁用Fast forward
> #因为本次合并要创建一个新的commit，所以加上-m参数，把commit描述写进去。
> Merge made by the 'recursive' strategy.
>  README.md | 1 +
>  1 file changed, 1 insertion(+)
> chenxushu@chenxushu:~/Desktop/clonegithub$ git log --graph
> ```
>
> 总结：
>
> - master分支应该是非常稳定的，仅仅使用master分支发布版本，平时不在上面干活
> - 比如：每个人都在dev的分支上干活，每个人都有自己的分支，时不时的向dev上合并代码就可以了
> - 比如：发布1.0版本，再把dev上的代码合并到master上面
> - 合并分支时，加上--no-ff参数表示使用普通模式进行合并，合并之后可以查看历史 记录，而Fast-Forword快速模式没有历史记录

### 上堂回顾

> 安装git
>
> ​	sudo apt-get install git
>
> 创建版本库【本地版本库】
>
> ​	普通目录，git init
>
> ​	创建文件在工作区，git  add filename    git commit -m "日志描述"
>
> 时光穿梭机
>
> ​	版本回退：git reset --hard  HEAD^    或者git reset --hard  commit  id
>
> ​	工作区/版本库/暂存区
>
> ​	管理修改：git status   /    git diff    HEAD  --    filename :查看版本库和工作区之间的不同
>
> ​	撤销修改：
>
> ​		a.修改了工作区中的文件，但是还没有add
>
> ​			git checkout -- filename  :丢弃工作区的修改
>
> ​		b.修改了工作区中的文件，add到暂存区，但是还没有commit
>
> ​		   	git  reset HEAD    filename：丢弃暂存区的修改
>
> ​			git checkout -- filename
>
> ​		c.修改了工作区中的文件,并add，commit
>
> ​			回退版本
>
> ​	删除文件：
>
> ​		删除工作区中的文件：rm filename
>
> ​		删除版本库中的文件：git rm filename	
>
> 远程仓库
>
> ​	添加ssh key【建立当前计算机和远程仓库之间的连接】
>
> ​	添加远程仓库：先有本地仓库，然后根据本地仓库创建远程仓库
>
> ​		git remote add origin  git@github.com:username/learngit.git:建立班底和远程仓库之间的连接
>
> ​		git push -u origin  master:将当前的master分支推送到远程仓库
>
> ​		git push  origin  master：以后再修改之后，可以再次推送
>
> ​	克隆仓库：先有远程仓库，然后将远程仓库克隆到本地
>
> ​		git clone git@github.com:username/clonegit.git
>
> 分支管理			
>
> ​	创建并切换分支：git checkout -b dev
>
> ​	切换分支：git checkout  dev
>
> ​	查看分支：git branch
>
> ​	合并到master：切换到master分支，执行命令git merge dev

#### 6.分支管理

##### 6.4bug分支

> 一般情况下，每个bug都需要使用一个分支来进行解决，解决后，分支删除
>
> git stash:可以把当前工作现场储存起来，然后先进行其他额的工作，完成工作之后，可以解封继续工作
>
> ```python
> 演示命令：
> rock@rockrong:~/Desktop$ git clone git@github.com:yangyang-git/day5Text.git
> 正克隆到 'day5Text'...
> remote: Counting objects: 3, done.
> remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
> 接收对象中: 100% (3/3), 完成.
> rock@rockrong:~/Desktop$ cd day5Text/
> rock@rockrong:~/Desktop/day5Text$ git branch
> * master
> rock@rockrong:~/Desktop/day5Text$ git checkout -b dev
> 切换到一个新分支 'dev'
> rock@rockrong:~/Desktop/day5Text$ git branch
> * dev
>   master
> rock@rockrong:~/Desktop/day5Text$ git status
> 位于分支 dev
> 无文件要提交，干净的工作区
> rock@rockrong:~/Desktop/day5Text$ vim README.md 
> rock@rockrong:~/Desktop/day5Text$ git add README.md 
> rock@rockrong:~/Desktop/day5Text$ git status
> 位于分支 dev
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	修改：     README.md
> 
> rock@rockrong:~/Desktop/day5Text$ git stash
> 
> *** 请告诉我你是谁。
> 
> 运行
> 
>   git config --global user.email "you@example.com"
>   git config --global user.name "Your Name"
> 
> 来设置您账号的缺省身份标识。
> 如果仅在本仓库设置身份标识，则省略 --global 参数。
> fatal: 无法自动探测邮件地址（得到 'rock@rockrong.(none)'）
> 无法保存当前索引状态
> rock@rockrong:~/Desktop/day5Text$ git config --global user.email "18501970795@163.com"
> rock@rockrong:~/Desktop/day5Text$ git config --global user.name "yangyang-git"
> rock@rockrong:~/Desktop/day5Text$ git stash			#封存工作现场
> 保存工作目录和索引状态 WIP on dev: e742319 Initial commit
> rock@rockrong:~/Desktop/day5Text$ git status
> 位于分支 dev
> 无文件要提交，干净的工作区
> rock@rockrong:~/Desktop/day5Text$ git checkout master
> 切换到分支 'master'
> 您的分支与上游分支 'origin/master' 一致。
> rock@rockrong:~/Desktop/day5Text$ git checkout -b bug-01
> 切换到一个新分支 'bug-01'
> rock@rockrong:~/Desktop/day5Text$ vim README.md 
> rock@rockrong:~/Desktop/day5Text$ git add README.md 
> rock@rockrong:~/Desktop/day5Text$ git commit -m "fixed a bug"
> [bug-01 235be14] fixed a bug
>  1 file changed, 2 insertions(+), 1 deletion(-)
> rock@rockrong:~/Desktop/day5Text$ git checkout master
> 切换到分支 'master'
> 您的分支与上游分支 'origin/master' 一致。
> rock@rockrong:~/Desktop/day5Text$ git merge --no-ff -m "merge bug-01" bug-01
> Merge made by the 'recursive' strategy.
>  README.md | 3 ++-
>  1 file changed, 2 insertions(+), 1 deletion(-)
> rock@rockrong:~/Desktop/day5Text$ git branch -d bug-01
> 已删除分支 bug-01（曾为 235be14）。
> rock@rockrong:~/Desktop/day5Text$ git status
> 位于分支 master
> 您的分支领先 'origin/master' 共 2 个提交。
>   （使用 "git push" 来发布您的本地提交）
> 
> 无文件要提交，干净的工作区
> rock@rockrong:~/Desktop/day5Text$ git stash list
> stash@{0}: WIP on dev: e742319 Initial commit
> rock@rockrong:~/Desktop/day5Text$ git stash pop      #解封，有冲突，解决冲突
> 自动合并 README.md
> 冲突（内容）：合并冲突于 README.md
> rock@rockrong:~/Desktop/day5Text$ vim README.md 
> rock@rockrong:~/Desktop/day5Text$ git stash pop
> README.md: needs merge
> 无法刷新索引
> rock@rockrong:~/Desktop/day5Text$ git commit -m "continue"
> U	README.md
> error: 无法提交，因为您有未合并的文件。
> 提示：请在工作区改正文件，然后酌情使用 'git add/rm <文件>' 命令标记
> 提示：解决方案并提交。
> fatal: 因为存在未解决的冲突而退出。
> rock@rockrong:~/Desktop/day5Text$ git add README.md 	#冲突解决之后需要再次add和commit
> rock@rockrong:~/Desktop/day5Text$ git commit -m "continue"
> 位于分支 master
> 您的分支领先 'origin/master' 共 2 个提交。
>   （使用 "git push" 来发布您的本地提交）
> 
> 无文件要提交，干净的工作区
> rock@rockrong:~/Desktop/day5Text$ git branch
>   dev
> * master
> rock@rockrong:~/Desktop/day5Text$ git checkout -b feature1
> 切换到一个新分支 'feature1'
> rock@rockrong:~/Desktop/day5Text$ touch a.txt
> rock@rockrong:~/Desktop/day5Text$ git add a.txt 
> rock@rockrong:~/Desktop/day5Text$ git commit -m "create a.txt"
> [feature1 120a22f] create a.txt
>  1 file changed, 0 insertions(+), 0 deletions(-)
>  create mode 100644 a.txt
> rock@rockrong:~/Desktop/day5Text$ git status
> 位于分支 feature1
> 无文件要提交，干净的工作区
> rock@rockrong:~/Desktop/day5Text$ vim a.txt 
> rock@rockrong:~/Desktop/day5Text$ git add a.txt 
> rock@rockrong:~/Desktop/day5Text$ git status
> ```
>
> 总结：
>
> ​	修复bug时，创建一个新的分支，进行bug的修复，然后合并，最后删除
>
> ​	当手头的工作没有完成的时候，使用git stash 将内容封存，然后取修复bug，当bug修复完成之后，则使用命令git stash pop解封

##### 6.5feature分支

> ```python
> 演示命令：
> rock@rockrong:~/Desktop/day5Text$ git branch
>   dev
> * master
> rock@rockrong:~/Desktop/day5Text$ git checkout -b feature1
> 切换到一个新分支 'feature1'
> rock@rockrong:~/Desktop/day5Text$ touch a.txt
> rock@rockrong:~/Desktop/day5Text$ git add a.txt 
> rock@rockrong:~/Desktop/day5Text$ git commit -m "create a.txt"
> [feature1 120a22f] create a.txt
>  1 file changed, 0 insertions(+), 0 deletions(-)
>  create mode 100644 a.txt
> rock@rockrong:~/Desktop/day5Text$ git status
> 位于分支 feature1
> 无文件要提交，干净的工作区
> rock@rockrong:~/Desktop/day5Text$ vim a.txt 
> rock@rockrong:~/Desktop/day5Text$ git add a.txt 
> rock@rockrong:~/Desktop/day5Text$ git status
> 位于分支 feature1
> 要提交的变更：
>   （使用 "git reset HEAD <文件>..." 以取消暂存）
> 
> 	修改：     a.txt
> 
> rock@rockrong:~/Desktop/day5Text$ git commit -m "add hello"
> [feature1 af31c25] add hello
>  1 file changed, 1 insertion(+)
> rock@rockrong:~/Desktop/day5Text$ git checkout dev
> 切换到分支 'dev'
> rock@rockrong:~/Desktop/day5Text$ git branch -d feature1	#正常删除
> error: 分支 'feature1' 没有完全合并。
> 如果您确认要删除它，执行 'git branch -D feature1'。
> rock@rockrong:~/Desktop/day5Text$ git branch -D feature1	#强制删除
> 已删除分支 feature1（曾为 af31c25）。
> ```
>
> 总结：
>
> ​	每开发一个新的功能【版本迭代】，最好新建一个分支来进行操作
>
> ​	如果需要丢弃一个还没有被合并的分支，使用命令 git branch -D  branch-name

##### 6.6多人协作

> 当你从远程仓克隆时，实际上git将本地的master和远程的master对应起来了，并且远程仓库的默认的名字为origin
>
> ```python
> 演示命令：
> rock@rockrong:~/Desktop/day5Text$ git remote     #查看远程库的信息
> origin
> rock@rockrong:~/Desktop/day5Text$ git remote -v
> origin	git@github.com:yangyang-git/day5Text.git (fetch)
> origin	git@github.com:yangyang-git/day5Text.git (push)
> ```

##### 1>推送分支

> 推送分支：把该分支上的所有的本地提交推送到远程库，推送时，要指定本地分支
>
> ```python
> 演示命令：
> rock@rockrong:~/Desktop/day5Text$ git branch
> * dev
>   master
> rock@rockrong:~/Desktop/day5Text$ git push origin master
> 对象计数中: 4, 完成.
> Delta compression using up to 2 threads.
> 压缩对象中: 100% (2/2), 完成.
> 写入对象中: 100% (4/4), 340 bytes | 340.00 KiB/s, 完成.
> Total 4 (delta 1), reused 0 (delta 0)
> remote: Resolving deltas: 100% (1/1), done.
> To github.com:yangyang-git/day5Text.git
>    e742319..cc4bef3  master -> master
> rock@rockrong:~/Desktop/day5Text$ git push origin dev
> Total 0 (delta 0), reused 0 (delta 0)
> To github.com:yangyang-git/day5Text.git
>  * [new branch]      dev -> dev
> rock@rockrong:~/Desktop/day5Text$ vim README.md 
> rock@rockrong:~/Desktop/day5Text$ git add README.md 
> rock@rockrong:~/Desktop/day5Text$ git commit -m "hello"
> [dev ae20ec5] hello
>  1 file changed, 2 insertions(+), 1 deletion(-)
> rock@rockrong:~/Desktop/day5Text$ git checkout master
> 切换到分支 'master'
> 您的分支与上游分支 'origin/master' 一致。
> rock@rockrong:~/Desktop/day5Text$ git merge dev
> 自动合并 README.md
> 冲突（内容）：合并冲突于 README.md
> 自动合并失败，修正冲突然后提交修正的结果。
> rock@rockrong:~/Desktop/day5Text$ vim README.md 
> rock@rockrong:~/Desktop/day5Text$ git add README.md 
> rock@rockrong:~/Desktop/day5Text$ git commit -m "conflict"
> [master 56411e2] conflict
> rock@rockrong:~/Desktop/day5Text$ git merge dev
> 已经是最新的。
> rock@rockrong:~/Desktop/day5Text$ git push origin dev
> 对象计数中: 3, 完成.
> 写入对象中: 100% (3/3), 255 bytes | 255.00 KiB/s, 完成.
> Total 3 (delta 0), reused 0 (delta 0)
> To github.com:yangyang-git/day5Text.git
>    e742319..ae20ec5  dev -> dev
> ```
>
> 总结：
>
> ​	并不是所有的分支都需要推送到远程仓库
>
> ​	a.master分支时主分支，因此要时刻与远程保持同步
>
> ​	b.dev是一个开发分支，团队所有的成员都在上面工作，所以也需要推送到远程仓库
>
> ​	c.bug分支只是修复一个bug，就没必要推送到远程

##### 2>抓取分支

> ```python
> 演示命令：
> rock@rockrong:~/Desktop/day5Text$ cd ..
> rock@rockrong:~/Desktop$ mkdir other
> rock@rockrong:~/Desktop$ cd other/
> rock@rockrong:~/Desktop/other$ git clone git@github.com:yangyang-git/day5Text.git
> 正克隆到 'day5Text'...
> remote: Counting objects: 10, done.
> remote: Compressing objects: 100% (3/3), done.
> remote: Total 10 (delta 2), reused 6 (delta 1), pack-reused 0
> 接收对象中: 100% (10/10), 完成.
> 处理 delta 中: 100% (2/2), 完成.
> rock@rockrong:~/Desktop/other$ cd day5Text/
> rock@rockrong:~/Desktop/other/day5Text$ git branch
> * master
> rock@rockrong:~/Desktop/other/day5Text$ git chckout -b dev origin/dev
> git：'chckout' 不是一个 git 命令。参见 'git --help'。
> 
> 最相似的命令是
> 	checkout
> rock@rockrong:~/Desktop/other/day5Text$ git checkout -b dev origin/dev
> 分支 'dev' 设置为跟踪来自 'origin' 的远程分支 'dev'。
> 切换到一个新分支 'dev'
> rock@rockrong:~/Desktop/other/day5Text$ git branch
> * dev
>   master
> rock@rockrong:~/Desktop/other/day5Text$ touch b.txt
> rock@rockrong:~/Desktop/other/day5Text$ vim b.txt 
> rock@rockrong:~/Desktop/other/day5Text$ git add b.txt 
> rock@rockrong:~/Desktop/other/day5Text$ git commit -m "b"
> [dev b08d6ec] b
>  1 file changed, 1 insertion(+)
>  create mode 100644 b.txt
> rock@rockrong:~/Desktop/other/day5Text$ git push origin dev    #推送分支
> 对象计数中: 3, 完成.
> Delta compression using up to 2 threads.
> 压缩对象中: 100% (2/2), 完成.
> 写入对象中: 100% (3/3), 274 bytes | 274.00 KiB/s, 完成.
> Total 3 (delta 0), reused 0 (delta 0)
> To github.com:yangyang-git/day5Text.git
>    ae20ec5..b08d6ec  dev -> dev
> rock@rockrong:~/Desktop/other/day5Text$ cd ../..
> rock@rockrong:~/Desktop$ cd day5Text/
> rock@rockrong:~/Desktop/day5Text$ git branch
>   dev
> * master
> rock@rockrong:~/Desktop/day5Text$ git checkout dev
> 切换到分支 'dev'
> rock@rockrong:~/Desktop/day5Text$ git pull
> remote: Counting objects: 3, done.
> remote: Compressing objects: 100% (2/2), done.
> remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
> 展开对象中: 100% (3/3), 完成.
> 来自 github.com:yangyang-git/day5Text
>    ae20ec5..b08d6ec  dev        -> origin/dev
> 当前分支没有跟踪信息。
> 请指定您要合并哪一个分支。
> 详见 git-pull(1)。
> 
>     git pull <远程> <分支>
> 
> 如果您想要为此分支创建跟踪信息，您可以执行：#抓取失败，根据提示操作，原因是没有指定本地dev分支与远程origin/dev分支的链接
> 
>     git branch --set-upstream-to=origin/<分支> dev
> 
> rock@rockrong:~/Desktop/day5Text$ git branch --set-upstream-to=origin/dev dev
> 分支 'dev' 设置为跟踪来自 'origin' 的远程分支 'dev'。		#设置跟踪
> rock@rockrong:~/Desktop/day5Text$ git pull       #抓取分支
> 更新 ae20ec5..b08d6ec
> Fast-forward
>  b.txt | 1 +
>  1 file changed, 1 insertion(+)
>  create mode 100644 b.txt
>   
> #此时，两个小伙伴之间就可以各自工作了，然后只需要将各自的修改每次提交到dev分支
> rock@rockrong:~/Desktop/day5Text$ vim b.txt
> rock@rockrong:~/Desktop/day5Text$ git add b.txt 
> rock@rockrong:~/Desktop/day5Text$ git commit -m "hello"
> [dev 61c1d88] hello
>  1 file changed, 1 insertion(+)
> rock@rockrong:~/Desktop/day5Text$ git push origin dev
> 对象计数中: 3, 完成.
> Delta compression using up to 2 threads.
> 压缩对象中: 100% (2/2), 完成.
> 写入对象中: 100% (3/3), 284 bytes | 284.00 KiB/s, 完成.
> Total 3 (delta 0), reused 0 (delta 0)
> To github.com:yangyang-git/day5Text.git
>    b08d6ec..61c1d88  dev -> dev
> rock@rockrong:~/Desktop/day5Text$ cd ..
> rock@rockrong:~/Desktop$ cd other/day5Text/
> rock@rockrong:~/Desktop/other/day5Text$ git pull
> remote: Counting objects: 3, done.
> remote: Compressing objects: 100% (2/2), done.
> remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
> 展开对象中: 100% (3/3), 完成.
> 来自 github.com:yangyang-git/day5Text
>    b08d6ec..61c1d88  dev        -> origin/dev
> 更新 b08d6ec..61c1d88
> Fast-forward
>  b.txt | 1 +
>  1 file changed, 1 insertion(+)
> rock@rockrong:~/Desktop/other/day5Text$ cat b.txt 
> fghajdfja
> hello
> 
>     
>  #注意：如果合并有冲突，需要手动解决，解决的方法和分支管理中的解决冲突完全一样。解决后，提交，再push
> #实际的工作流程是：先pull[抓取]，后push[推送]
> ```
>
> 总结：
>
> ​	a.查看远程库的信息，使用git remote -v
>
> ​	b.本地新建的分支如果不推送到远程，对其他人都是不可见的
>
> ​	c.从本地推送分支，使用命令git push origin branchname,如果推送失败，则先用git pull抓取
>
> ​	d.在本地创建于远程分支的连接，使用命令git checkout -b branchname origin/branchname
>
> ​	e。从远程抓取分支，使用git pull，如果有冲突，则要先解决冲突	

#### 7.标签管理

##### 7.1创建标签

> ```python
> 演示命令：
> rock@rockrong:~/Desktop/day5Text$ git tag v1.0	#创建标签，默认创建的是当前最新提交的标签
> rock@rockrong:~/Desktop/day5Text$ git tag
> v1.0
> rock@rockrong:~/Desktop/day5Text$ git tag v0.2 ae20ec5	#为指定commit id创建标签
> rock@rockrong:~/Desktop/day5Text$ git tag
> v0.2
> v1.0
> ```

##### 7.2操作标签

> ```python
> 演示命令：
> rock@rockrong:~/Desktop/day5Text$ git show v1.0	#查看指定标签的详细信息
> commit 61c1d8863fd7df3d20c156ace3bfa1d7882b636c (HEAD -> dev, tag: v1.0, origin/dev)
> Author: yangyang-git <18501970795@163.com>
> Date:   Mon Jul 2 10:52:50 2018 +0800
> 
>     hello
> 
> diff --git a/b.txt b/b.txt
> index 9022bb8..4bc9d07 100644
> --- a/b.txt
> +++ b/b.txt
> @@ -1 +1,2 @@
>  fghajdfja
> +hello
> rock@rockrong:~/Desktop/day5Text$ git tag -a v0.1 -m "version 0.1" e7423195
>   #创建标签，携带标签的描述信息
> rock@rockrong:~/Desktop/day5Text$ git tag	#查看当前分支下的标签
> v0.1
> v0.2
> v1.0
> rock@rockrong:~/Desktop/day5Text$ git tag -d v0.1	
> 已删除标签 'v0.1'（曾为 97026a8）
> rock@rockrong:~/Desktop/day5Text$ git push origin --tags	#将本地仓库中的标签推送到远程仓库
> Total 0 (delta 0), reused 0 (delta 0)
> To github.com:yangyang-git/day5Text.git
>  * [new tag]         v0.2 -> v0.2
>  * [new tag]         v1.0 -> v1.0
> rock@rockrong:~/Desktop/day5Text$ git tag -d v0.2		#删除本地仓库中的标签
> 已删除标签 'v0.2'（曾为 ae20ec5）
> rock@rockrong:~/Desktop/day5Text$ git push origin :refs/tags/v0.2To
>     #删除远程仓库中的指定标签
> remote: warning: Deleting a non-existent ref.
> To github.com:yangyang-git/day5Text.git
>  - [deleted]         v0.2To
> ```

### 十、shell编程

#### 1.简介

##### 1.1什么是shell

> 把在终端运行的命令保存到文件中，这个文件就是shell程序
>
> 简单的说，shell编程就是第Linux命令的逻辑化处理

##### 1.2shell解析器的类型

> bash，ash，ksh等，默认使用bash
>
> ```
> 演示命令：
> echo $SHELL
> /bin/bash
> ```

##### 1.3shell的作用

> 如果需要反复执行某些Linux命令，则可以将这些命令写到一个shell脚本中，然后每次只需要运行一下这个脚本即可

#### 2.第一个shell程序

##### 2.1实现

> 打开文本编辑器(可以使用 tou'ch命令来创建文件)，新建一个文件 test.sh，扩展名为 sh（sh代表shell），扩展名并不影响脚本执行，见名知意就好
>
> 代码演示：
>
> ```shell
> #!/bin/bash
> #打印hello world
> echo "Hello World !"
> ```

##### 2.2运行

> 方式一：作为可执行程序
>
> ```python
> touch test.sh
> vim test.sh
> chmod +x ./test.sh
> ./test.sh
> ```
>
> 方式二：作为解释器参数
>
> ```python
> bin/bash test.sh 
> ```

#### 3.shell中的变量

##### 3.1变量的定义

> 定义：变量名=值
>
> ```shell
> 演示命令：
> your_name="zhangsan"
> echo $your_name
> num=10
> echo ${num}
> 
> #注意：变量名外面的花括号是可选的，加不加都行，加花括号是为了帮助解释器识别变量的边界
> echo "his name is ${your_name}"
> ```

##### 3.2只读变量

> readonly：只读，将变量声明为readonly，只读变量的值不能发生改变
>
> ```shell
> myUrl="http://www.baidu.com"
> readonly myUrl
> myUrl="http://www.1000phone.com"
> 
> #运行脚本,报错：/bin/sh: NAME: This variable is read only
> ```

##### 3.3删除变量

> unset：删除变量
>
> ```shell
> 代码演示：
> myUrl="http://www.baidu.com"
> unset myUrl
> echo $myUrl
> 
> #变量被删除后不能再次使用。unset 命令不能删除只读变量。
> #以上实例执行将没有任何输出
> ```

#### 4.字符串和数组

##### 4.1字符串

> 双引号或者单引号
>
> 单引号的限制：
>
> ​	a.单引号中的任何字符都会原样输出，单引号字符串中的变量是无效的
>
> ​	b.单引号字符串中不能再出现单引号【对单引号进行转义后去不起作用】
>
> 总结：
>
> ​	双引号：可以包含除了$、`、\、‘‘之外的任意字符
>
> ​	单引号：其中的任意字符都不会被解析，都会原样输出
>
> ​	反引号：会将其中的内容作为命令执行
>
> ​	反斜线：转义特定的字符，如：&、*、^、等
>
> 代码演示:
>
> ```shell
> 代码演示：
> #!/bin/bash
> 
> #定义字符串
> your_name='qinjx'
> str="Hello, I know you are \"$your_name\"! \n"
> 
> #拼接字符串
> your_name="qinjx"
> greeting="hello, "$your_name" !"
> greeting_1="hello, ${your_name} !"
> echo $greeting $greeting_1
> 
> #获取字符串长度
> string="abcd"
> echo ${#string} #输出 4
> 
> #提取子字符串
> string="1000phone is a great site"
> echo ${string:1:4}       #包头包尾
> 
> #查找子字符串
> string="1000phone is a great company"
> echo `expr index "$string" is`  
> 
> #注意： 以上脚本中 "`" 是反引号，而不是单引号 "'"，不要看错了哦
> ```

##### 4.2数组

> bash只支持一维数组，不支持多维数组
>
> 并没有限制数组的大小
>
> 数组元素的下标也是从0开始的，获取数组中的元素使用下标
>
> 定义数组：数组名=(值1 值2 值3....)
>
> 注意：shell中的数组元素之间使用空格分隔
>
> 代码演示：
>
> ```shell
> #数组的定义
> arr1=(10 20 30 40)
> echo $arr1
> arr2=(
> 10
> 20
> 30
> 40
> )
> echo $arr2
> 
> #数组的使用
> #读取数组中的元素
> echo ${arr1[2]}
> #如果要读取数组中的全部元素
> echo ${arr2[@]}
> 
> # 取得数组元素的个数
> length=${#arr1[@]}
> echo $length
> # 或者
> length=${#arr1[*]}
> echo $length
> # 取得数组单个元素的长度
> lengthn=${#arr1[3]}
> echo $lengthn
> ```

#### 5.shell中的运算符

> expr:是一款表达式计算工具，使用它能够完成表达式的求值操作
>
> 代码演示：
>
> ```shell
> val=`expr 1 + 2`
> echo "两数之和为 : $val"
> 
> #1.算术运算符
> val=`expr $a + $b`
> echo "a + b : $val"
> 
> val=`expr $a \* $b`
> echo "a * b : $val"
> 
> #2.关系运算符
> ## []中，前后都需要空格
> if [ $a -eq $b ]
> then
>    echo "$a -eq $b : a 等于 b"
> else
>    echo "$a -eq $b: a 不等于 b"
> fi
> 
> #3.逻辑运算符
> if [ 1 -lt 3 ] && [ 2 -lt 3 ]; 
> then
> 	echo "ok"
> fi
> ```

#### 6.echo、printf、test命令

> 1>echo
>
> ```shell
> echo -e "OK! \n" 		# -e 开启转义,\n 显示换行
> echo -e "OK! \c"		 # -e 开启转义 \c 不换行
> 
> echo `date`    #显示命令执行结果
> #注意： 这里使用的是反引号 `, 而不是单引号 '。
> #结果为：Thu Jul 24 10:08:46 CST 2014
> ```
>
> 2>printf
>
> ```shell
> printf "%-10s %-8s %-4s\n" 姓名 性别 体重kg  
> printf "%-10s %-8s %-4.2f\n" 张三 男 66.1234 
> printf "%-10s %-8s %-4.2f\n" 李四 男 48.6543 
> ```
>
> 注意：
>
> ​	%s %d %f都是格式替换符
>
> ​	-10s:指的是一个宽度为10的字符（-表示左对齐，没有则表示右对齐），任何字符都会填充在这10个字符内，如果不足则使用空格自动填充
>
> ​	-4.2f:指的是格式化为小数，其中.2表示保留小数点后两位
>
> 3>test
>
> ```shell
> #1.数值测试
> num1=100
> num2=100
> if test $[num1] -eq $[num2]
> then
>     echo '两个数相等！'
> else
>     echo '两个数不相等！'
> fi
> 
> #2.字符串测试
> num1="hello"
> num2="hello11"
> if test $num1 = $num2
> then
>     echo '两个字符串相等!'
> else
>     echo '两个字符串不相等!'
> fi
> 
> #3.文件测试
> cd /bin
> if test -e ./bash
> then
>     echo '文件已存在!'
> else
>     echo '文件不存在!'
> fi
> ```
>
> test命令用来监测某个条件是否成立，他可以进行数值，字符和文件的监测

#### 7.shell中的流程控制语句

##### 7.1分支语句

> if，case
>
> 代码演示：
>
> ```shell
> #if语句
> #单分支
> if [ 1 -lt 3 ] && [ 2 -lt 3 ]; 
> then
> 	echo "ok"
> fi
> 
> #双分支
> num1=$[2*3]
> num2=$[1+5]
> #if else语句经常与test命令结合使用
> if test $[num1] -eq $[num2]
> then
>     echo '两个数字相等!'
> else
>     echo '两个数字不相等!'
> fi
> 
> #多分支
> a=10
> b=20
> if [ $a == $b ]
> then
>    echo "a 等于 b"
> elif [ $a -gt $b ]
> then
>    echo "a 大于 b"
> elif [ $a -lt $b ]
> then
>    echo "a 小于 b"
> else
>    echo "没有符合的条件"
> fi
> 
> 
> #until语句
> echo '输入 1 到 4 之间的数字:'
> echo '你输入的数字为:'
> read aNum
> case $aNum in
>     1)  echo '你选择了 1'
>     ;;
>     2)  echo '你选择了 2'
>     ;;
>     3)  echo '你选择了 3'
>     ;;
>     4)  echo '你选择了 4'
>     ;;
>     *)  echo '你没有输入 1 到 4 之间的数字'
>     ;;
> esac
> ```

##### 7.2循环语句

> for while    until
>
> 代码演示：
>
> ```shell
> #for语句
> #需求：顺序输出当前列表中的数字
> for num in 1 2 3 4 5
> do
>     echo "The value is: $num"
> done
> 
> 
> #需求：顺序输出字符串中的字符
> for str in 'This is a string'
> do
>     echo $str
> done
> 
> #需求：遍历数组中的所有元素
> a=(1 2 3)
>   for x in ${a[*]}
>   do 
>   	echo $x
>   done
>   
> #while语句
> #需求：输出数字1到5
> int=1
> while(( $int<=5 ))
> do
>     echo $int
>     let "int++"
> done
> 
> 
> #需求：求1~10之间所有整数的和
> i=1
> sum=0
> 
> while [ $i -le 10 ]
> do
>   	sum=$[$sum+$i]
> 
>   	i=$[$i+1]
> done
> echo $sum
> 
> #until语句
> i=1
> 
> until [ $i -gt 10 ]
> do
> 	echo $i
> 	((i++))
> done
> ```

#### 8.函数

> 代码演示：
>
> ```shell
> #无参无返回值
> #定义函数
> demo()
> {
> 	echo 'hello world'
> }
> #调用函数
> demo
> 
> #有返回值
> funWithReturn(){
>     echo "输入第一个数字: "
>     read aNum
>     echo "输入第二个数字: "
>     read anotherNum
>     return $(($aNum+$anotherNum))
> }
> funWithReturn
> echo  $? 
> 
> #有参有返回值
> arg()
> {
> 	echo $1
> 	echo $2
> 	echo $#
> 	echo $*
> 	return 123
> }
> 
> arg 1 2
> # $? 表示函数的返回值
> echo $?
> ```

