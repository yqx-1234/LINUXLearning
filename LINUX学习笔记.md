## LINUX系统学习笔记(javaEE、大数据、Python开发通用)

#### 一.LINUX学习方向

![](E:\learning\LINUXLearning\IMAGES\1_1.png)



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

![](E:\learning\LINUXLearning\IMAGES\3_1.png)

4.常见的操作系统：windows,linux,android



#### 四.Linux与Unix的关系

#### 五.windows与linux的关系

![](E:\learning\LINUXLearning\IMAGES\5_1.png)



#### 六.VM与LINUX的安装

##### 1.搭建环境

1.先安装virtual machine,vm12(虚拟机)

2.再安装Linux（CentOS6.8）

3.关系图

![](E:\learning\LINUXLearning\IMAGES\6_2.png)

##### 2.vm12和CentOS系统的安装

![](E:\learning\LINUXLearning\IMAGES\6_3.png)

###### 1.vm12安装步骤

![](E:\learning\LINUXLearning\IMAGES\6_4.png)

进入BIOS设置虚拟化

安装vm12步骤

![](E:\learning\LINUXLearning\IMAGES\6_5.png)



###### 2.CentOS的安装

1.创建虚拟机(空间)

1.主页->创建新的虚拟机

![](E:\learning\LINUXLearning\IMAGES\7_1.png)

![](E:\learning\LINUXLearning\IMAGES\7_2.png)

![](E:\learning\LINUXLearning\IMAGES\7_3.png)

![](E:\learning\LINUXLearning\IMAGES\7_4.png)

![](E:\learning\LINUXLearning\IMAGES\7_5.png)

![](E:\learning\LINUXLearning\IMAGES\7_6.png)

![](E:\learning\LINUXLearning\IMAGES\7_7.png)

![](E:\learning\LINUXLearning\IMAGES\7_8.png)

![](E:\learning\LINUXLearning\IMAGES\7_9.png)

![](E:\learning\LINUXLearning\IMAGES\7_10.png)



难点：

1.虚拟机的网络连接三种形式说明：

​	桥接模式：同一个网络环境下，各个主机可以任意访问其他主机即其所有的虚拟机。好处：Linux可以和其他系统通信。弊端：容易出现IP地址冲突

![](E:\learning\LINUXLearning\IMAGES\7_11.png)

​	NAT模式：母机双IP，母机不能与其他母机所有的Linux虚拟机通信，但母机所有的Linux虚拟机可以和其他母机通信，网络地址转换方式：Linux可以访问外网，不会造成IP冲突

![](E:\learning\LINUXLearning\IMAGES\7_12.png)

​	主机模式：你的Linux 是一个独立的主机，不能访问外网



2.开始安装系统(CentOS6.8)

![](E:\learning\LINUXLearning\IMAGES\7_13.png)

![](E:\learning\LINUXLearning\IMAGES\7_14.png)

![](E:\learning\LINUXLearning\IMAGES\7_15.png)

![](E:\learning\LINUXLearning\IMAGES\7_16.png)

![](E:\learning\LINUXLearning\IMAGES\7_17.png)

![](E:\learning\LINUXLearning\IMAGES\7_18.png)

![](E:\learning\LINUXLearning\IMAGES\7_19.png)

![](E:\learning\LINUXLearning\IMAGES\7_20.png)

![](E:\learning\LINUXLearning\IMAGES\7_21.png)

![](E:\learning\LINUXLearning\IMAGES\7_22.png)

![](E:\learning\LINUXLearning\IMAGES\7_23.png)

![](E:\learning\LINUXLearning\IMAGES\7_24.png)

![](E:\learning\LINUXLearning\IMAGES\7_25.png)

![](E:\learning\LINUXLearning\IMAGES\7_26.png)

![](E:\learning\LINUXLearning\IMAGES\7_27.png)

![](E:\learning\LINUXLearning\IMAGES\7_28.png)

![](E:\learning\LINUXLearning\IMAGES\7_29.png)

然后格式化，修改磁盘

![](E:\learning\LINUXLearning\IMAGES\7_30.png)

![](E:\learning\LINUXLearning\IMAGES\7_31.png)

![](E:\learning\LINUXLearning\IMAGES\7_33.png)

![](E:\learning\LINUXLearning\IMAGES\7_35.png)

![](E:\learning\LINUXLearning\IMAGES\7_34.png)

![](E:\learning\LINUXLearning\IMAGES\7_36.png)

![](E:\learning\LINUXLearning\IMAGES\7_37.png)

![](E:\learning\LINUXLearning\IMAGES\7_38.png)

创建用户暂时先不创建，后面会单独创建，先使用root账户登录



![](E:\learning\LINUXLearning\IMAGES\7_39.png)

![](E:\learning\LINUXLearning\IMAGES\7_40.png)

![](E:\learning\LINUXLearning\IMAGES\7_41.png)

![](E:\learning\LINUXLearning\IMAGES\7_42.png)

![](E:\learning\LINUXLearning\IMAGES\7_43.png)

至此CentOS系统安装完成



安装CentOS时的注意事项：

LINUX密码生产中一定要设置的强度相当高，不然极易被破解，这里学习用：12243672

Linux分区：

必创建的三个分区

1./boot分区：Linux在启动时会生成引导文件，默认放在boot分区内

![](E:\learning\LINUXLearning\IMAGES\7_24.png)



2.swap分区：交换分区，当系统内存不够用时，可用此分区替代内存

![](E:\learning\LINUXLearning\IMAGES\7_27.png)

3.根分区：/

![](E:\learning\LINUXLearning\IMAGES\7_28.png)

![](E:\learning\LINUXLearning\IMAGES\7_29.png)

然后格式化，修改磁盘