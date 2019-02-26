1、环境和软件准备
(1) 检查服务器是否安装GNome
	rpm -qa | grep desktop
(2) CentOS 下
	使用如下命令，进行安装
	yum install tigervnc  
	yum install tigervnc-server 

(3) Windows 下
	https://tigervnc.org/		--进入tigervnc官网
	https://github.com/TigerVNC/tigervnc/releases		--下载

2、在要远程桌面连接的服务器启动vncserver（服务器端）
	vncserver :n	--这里的n是sessionnumber，不指定默认为1，也可以是2、3等等。第一次会提示输入密码，以后可以使用vncpasswd命令修改密码。
	在防火墙中放行端口5900 + n

3、启动vncviewer（客户端）
	linux	vncviewer localhost:n	--这里的n对应vncserver指定的数字
	windows	直接图形化操作

4、启动tigervnc的Windows版本（tigervnc-1.2.0.exe）
VNC的默认端口是5900，而远程桌面连接端口则是5900+n（n是vncserver命令指定的）。如果使用“vncserver :1”命令启动VNC Server，那么下面的端口应该是5901。

5、关闭vncserver（服务器端）
	vncserver -kill :n
	vncserver –list	--如果使用vncserver :n多次建立远程桌面
	vncserver -list	--列出当前用户建立的所有远程桌面，例如

参考资料：
	1、https://tigervnc.org/
	2、http://heather.cs.ucdavis.edu/~matloff/vnc.html
	3、http://blog.chinaunix.net/uid-26642180-id-3135447.html
	4、http://blog.csdn.net/daydreamingboy/article/details/8196747/#