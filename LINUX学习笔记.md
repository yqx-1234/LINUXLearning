## LINUX系统学习笔记(javaEE、大数据、Python开发通用)

#### 一.LINUX学习方向

![](.\IMAGES\1_1.png)



#### 二.LINUX应用方向

1.个人桌面应用(ubuntu)

2.服务器领域(最强)

3.嵌入式领域

#### 三.LINUX学习阶段和方法

##### 1.学习流程：

1.linux环境得基本操作命令

2.linux的各种配置

3.linux下如何搭建对应语言的开发环境

4.能编写shell脚本

看完课程前四个必须达到

5.能进行安全设置，防止攻击，保障服务器正常运行

6.深入理解linux系统（对内核有研究）

##### 2.学习思想

1.高效愉快的学习

2.先建立整体框架

3.只用掌握基本的Linux命令，要学会查询手册和百度

4.先know how ,再know why

5.重实操

6.适当囫囵吞枣

7.Linux不是编程，重点是实际操作，各种常用指令要玩溜



### LINUX基础篇——入门

#### 三.LINUX系统介绍

1.一款操作系统，免费，开源，安全，高效，稳定，处理高并发非常强悍，现在很多企业级都部署到Linux/unix服务器运行

2.Linux创始人：linux:林纳斯，吉祥物：企鹅:tux

3.Linux主要发行版本：Linux与Ubuntu、redhat等的关系：内核与应用

![](.\IMAGES\3_1.png)

4.常见的操作系统：windows,linux,android



#### 四.Linux与Unix的关系

#### 五.windows与linux的关系

![](.\IMAGES\5_1.png)



#### 六.VM与LINUX的安装

##### 1.搭建环境

1.先安装virtual machine,vm12(虚拟机)

2.再安装Linux（CentOS6.8）

3.关系图

![](.\IMAGES\6_2.png)

##### 2.vm12和CentOS系统的安装

![](.\IMAGES\6_3.png)

###### 1.vm12安装步骤

![](.\IMAGES\6_4.png)

进入BIOS设置虚拟化

安装vm12步骤

![](.\IMAGES\6_5.png)



###### 2.CentOS的安装

1.创建虚拟机(空间)

1.主页->创建新的虚拟机

![](.\IMAGES\7_1.png)

![](.\IMAGES\7_2.png)

![](.\IMAGES\7_3.png)

![](.\IMAGES\7_4.png)

![](.\IMAGES\7_5.png)

![](.\IMAGES\7_6.png)

![](.\IMAGES\7_7.png)

![](.\IMAGES\7_8.png)

![](.\IMAGES\7_9.png)

![](.\IMAGES\7_10.png)



难点：

1.虚拟机的网络连接三种形式说明：

​	桥接模式：同一个网络环境下，各个主机可以任意访问其他主机即其所有的虚拟机。好处：Linux可以和其他系统通信。弊端：容易出现IP地址冲突

![](.\IMAGES\7_11.png)

​	NAT模式：母机双IP，母机不能与其他母机所有的Linux虚拟机通信，但母机所有的Linux虚拟机可以和其他母机通信，网络地址转换方式：Linux可以访问外网，不会造成IP冲突

![](.\IMAGES\7_12.png)

​	主机模式：你的Linux 是一个独立的主机，不能访问外网



2.开始安装系统(CentOS6.8)

![](.\IMAGES\7_13.png)

![](.\IMAGES\7_14.png)

![](.\IMAGES\7_15.png)

![](.\IMAGES\7_16.png)

![](.\IMAGES\7_17.png)

![](.\IMAGES\7_18.png)

![](.\IMAGES\7_19.png)

![](.\IMAGES\7_20.png)

![](.\IMAGES\7_21.png)

![](.\IMAGES\7_22.png)

![](.\IMAGES\7_23.png)

![](.\IMAGES\7_24.png)

![](.\IMAGES\7_25.png)

![](.\IMAGES\7_26.png)

![](.\IMAGES\7_27.png)

![](.\IMAGES\7_28.png)

![](.\IMAGES\7_29.png)

然后格式化，修改磁盘

![](.\IMAGES\7_30.png)

![](.\IMAGES\7_31.png)

![](.\IMAGES\7_33.png)

![](.\IMAGES\7_35.png)

![](.\IMAGES\7_34.png)

![](.\IMAGES\7_36.png)

![](.\IMAGES\7_37.png)

![](.\IMAGES\7_38.png)

创建用户暂时先不创建，后面会单独创建，先使用root账户登录



![](.\IMAGES\7_39.png)

![](.\IMAGES\7_40.png)

![](.\IMAGES\7_41.png)

![](.\IMAGES\7_42.png)

![](.\IMAGES\7_43.png)

至此CentOS系统安装完成



安装CentOS时的注意事项：

LINUX密码生产中一定要设置的强度相当高，不然极易被破解，这里学习用：12243672

Linux分区：

必创建的三个分区

1./boot分区：Linux在启动时会生成引导文件，默认放在boot分区内

![](.\IMAGES\7_24.png)



2.swap分区：交换分区，当系统内存不够用时，可用此分区替代内存

![](.\IMAGES\7_27.png)

3.根分区：/

![](.\IMAGES\7_28.png)

![](.\IMAGES\7_29.png)

然后格式化，修改磁盘

#### 七.CentOS的终端使用与联网

##### 1.对终端的使用

![](.\IMAGES\7_44.png)

2.配置联网

![](.\IMAGES\8_1.png)

#### 八.VMtool的使用和安装

vmtools:让我们在windows下更好的管理vm虚拟机

1.可以直接粘贴命令在windows和centos之间

2.可以设置windows和centos的共享文件夹

![](.\IMAGES\8_2.png)

##### vmtools安装：

1.进入centos

2.点击vm菜单的->install vmware tools

3.centos会出现一个vm的安装包

4.点击右键解压，得到一个安装文件

5.进入该vm解压的目录，该文件在/root/桌面/vmware-tools-distrib/下

6.安装./vmware-install.pl

7.全部使用默认设置即可

8.需要reboot重新启动即可生效

解压命令：eg:tar -zxvf VMwareTools-10.0.5-3228253.tar.gz

指令安装

![](.\IMAGES\8_3.png)

然后一路回车就行

![](.\IMAGES\8_4.png)

安装完后进行重启

重启指令：reboot

然后就可以实现windows和centos之间内容的复制粘贴了

##### 共享文件夹：

![](.\IMAGES\8_5.png)

共享文件夹在Linux中的位置

![](.\IMAGES\8_6.png)



#### 九.Linux文件系统目录结构

基本介绍:采用级层式的树状目录结构，在此结构中的最上层是根目录"/",然后在此目录下再创建其他的目录,以文件的形式来管理设备

**“在Linux的世界中，一切皆文件”**

opt：安装软件所用的文件夹

![](.\IMAGES\9_1.png)



![](.\IMAGES\9_2.png)

![](.\IMAGES\9_3.png)

![](.\IMAGES\9_4.png)

![](.\IMAGES\9_5.png)

![](.\IMAGES\9_6.png)

#### 十.远程登录Linux服务器(xshell5)

这里使用xshell6:远程登录服务器

远程上传和下载文件软件:XFtp5

![](.\IMAGES\10_1.png)

使用前提：Linux需要开启sshd服务，该服务监听22号端口，一般情况下开启的。（端口：类似人的耳朵，理论上有65536个端口可以开启）端口开启越多，安全性越弱。

如何确定sshd服务是否开启？

1.setup

![](.\IMAGES\10_2.png)

2.选择系统服务，其中标“*”表示开启服务，查找sshd,看是否标星号。

![](.\IMAGES\10_3.png)

安好xshell6后新建一个会话：

注意点：LinuxIP地址查询：命令：ifconfig

未联网：无法得到IP地址

![](.\IMAGES\10_4.png)

需要联网才会分配IP地址

分配IP地址

![](.\IMAGES\10_5.png)

新建会话过程：

![](.\IMAGES\10_6.png)

![](.\IMAGES\10_7.png)



![](.\IMAGES\10_8.png)

![](.\IMAGES\10_9.png)



建立远程连接完成：

测试：

1.输入reboot即可远程重启系统

2.在Linux建立文件，是否可以被xshell监听到，以验证远程连接有效。

1.cd / home/#切换到home目录下

2.ll#查询该目录下的文件

3.touch hello#新建一个名为hello的文件

![](.\IMAGES\10_11.png)



#### 十一.XFTP7的安装与使用

XFTP7:远程上传和下载文件

##### 使用

1.新建会话

![](.\IMAGES\11_1.png)



连接成功

![](.\IMAGES\11_2.png)

文件的传输与下载：

![](.\IMAGES\11_3.png)



#### 十二.Vi和Vim编辑器的使用

Linux重要的编辑器

vi:Linux内建的编辑器

Vim:vi的增强版，可以主动的以字体颜色辨别语法的正确性

vi和vim常见的三种模型：

1.正常模式：默认模式，使用可以使用【上下左右】来移动光标和使用各种快捷键，可以删除字符或删除整行

2.插入模式(编辑模式):按i可进入

3.命令行模式:提供相关指令，完成存盘、读取、替换、读取、离开vim、显示行号等的动作

eg:使用vim开发一个：hello.java程序。

1.rm 123.txt %删除123.txt文件

2.ll:显示当前目录下的文件

3.Vim按i进入编辑模式，按Esc键退出编辑模式进入一般模式，再按：即可进去命令行模式

4.命令行模式下输入：wq表示写入文件并退出，输入“q"表示退出

![](.\IMAGES\12_3.png)

![](.\IMAGES\12_4.png)

![](.\IMAGES\12_5.png)

文件写入成功：

![](.\IMAGES\12_6.png)

![](.\IMAGES\12_7.png)



注：q:退出

​		q!:强制退出

**vi和vim的快捷键：**

![](.\IMAGES\12_8.png)

注意：

1.拷贝粘贴：再一般模式下输入yy即拷贝当前行，还需输入p才能粘贴当前行

2.编辑文件，使用快捷键到文档的最末行(G)和最首行(gg),注意是在正常模式(一般模式)下输入

3.撤销操作在正常模式下进行

4.移动光标操作也是在正常模式下完成

扩展阅读：

Vim快捷键键盘图：

![](.\IMAGES\12_9.png)



#### 十三.关机，重启，用户登录注销

##### 1.关机与重启指令：

**shutdown:**

shutdown -h now:表示立即关机

shutdown -h 1:表示1分钟后关机

shutdown -r now:表示立即重启

**halt:**

halt:效果等价于关机

**reboot:**

reboot:重启

**sync:**

sync:把内存数据同步到磁盘上

注：不管是重启系统还是关闭系统，首先要运行sync命令，把内存中的数据同步到磁盘上去



##### 2.用户的登陆和注销

1.登录是一般少用root账号登录，权限太高，一般方法是：利用普通用户登录，再用"su - 用户名"命令来切换成系统管理员身份

2.在提示符下输入logout即可注销用户

注：1.logout指令图形运行级别无效，在运行级别3下有效

注销用户：

![](.\IMAGES\13_1.png)

















































































































































































































































































