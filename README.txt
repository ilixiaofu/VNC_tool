1�����������׼��
(1) ���������Ƿ�װGNome
	rpm -qa | grep desktop
(2) CentOS ��
	ʹ������������а�װ
	yum install tigervnc  
	yum install tigervnc-server 

(3) Windows ��
	https://tigervnc.org/		--����tigervnc����
	https://github.com/TigerVNC/tigervnc/releases		--����

2����ҪԶ���������ӵķ���������vncserver���������ˣ�
	vncserver :n	--�����n��sessionnumber����ָ��Ĭ��Ϊ1��Ҳ������2��3�ȵȡ���һ�λ���ʾ�������룬�Ժ����ʹ��vncpasswd�����޸����롣
	�ڷ���ǽ�з��ж˿�5900 + n

3������vncviewer���ͻ��ˣ�
	linux	vncviewer localhost:n	--�����n��Ӧvncserverָ��������
	windows	ֱ��ͼ�λ�����

4������tigervnc��Windows�汾��tigervnc-1.2.0.exe��
VNC��Ĭ�϶˿���5900����Զ���������Ӷ˿�����5900+n��n��vncserver����ָ���ģ������ʹ�á�vncserver :1����������VNC Server����ô����Ķ˿�Ӧ����5901��

5���ر�vncserver���������ˣ�
	vncserver -kill :n
	vncserver �Clist	--���ʹ��vncserver :n��ν���Զ������
	vncserver -list	--�г���ǰ�û�����������Զ�����棬����

�ο����ϣ�
	1��https://tigervnc.org/
	2��http://heather.cs.ucdavis.edu/~matloff/vnc.html
	3��http://blog.chinaunix.net/uid-26642180-id-3135447.html
	4��http://blog.csdn.net/daydreamingboy/article/details/8196747/#