#####################################################################################
################ ����װ˵��ֻ������64λ��Windows����ϵͳ��Linux������ ###############
################ �Ƽ�ʹ�÷��������64λWindowsϵͳ                    ###############
#####################################################################################
=====================================================================================
==============================================����˵��===============================
�Ƽ���װ��E:/clusterĿ¼�������װ��E:/cluster��ֻҪ�޸�3��4��tomcat����Ŀ¼���ɡ�
�޸����������ļ���
1��apache2.4\conf\httpd.conf
�ҵ�37�У�
ServerRoot "E:/cluster/apache2.4"
�ҵ�241,242��
DocumentRoot "E:/cluster/apache2.4/htdocs"
<Directory "E:/cluster/apache2.4/htdocs">

����Щ·���޸ĳ����apache��Ŀ¼��

2��apache2.4\conf\extra\mod_jk.conf
�ҵ�16��
�������Լ�������ӳ�䴦����

3��tomcat1\conf\server.xml
�޸�147�У������е������޸ĳ����Ӧ�õ�·��
<Context path="/glaf" docBase="E:/cluster/WebContent" reloadable="false"/>

4��tomcat2\conf\server.xml
�޸�147�У������е������޸ĳ����Ӧ�õ�·��
<Context path="/glaf" docBase="E:/cluster/WebContent" reloadable="false"/>

5)�޸�ÿ��zookeeper��confĿ¼�µ�zoo.cfg
�ҵ�12�м�13��
�޸�E:/cluster�����Լ��İ�װĿ¼
dataDir=E:/cluster/zookeeper1/data
dataLogDir=E:/cluster/zookeeper1/logs
�����װ����̨���������޸�32��34��
server.1=localhost:2887:3887
server.2=localhost:2888:3888
server.3=localhost:2889:3889
��localhost�޸ĳ�ÿ��Server��Ӧ��ip��ַ��

=====================================================================================
==============================================��װ˵��===============================
1����װVC10
��������²���ϵͳ
Windows 7 SP1, 
Windows 8 / 8.1, 
Windows Vista SP2, 
Windows Server 2008 R2 SP1, 
Windows Server 2012 / R2
�밲װvc11redist_x64.exe
!!!!!!!!!!!!!!�����Ҫ��XP��2003�°�װ!!!!!!!!!!!
��ʹ��vc10redist_x64.exe

2����װapache����
ִ��apache2.4Ŀ¼�µ�apache_installservice.bat

3����װzookeeper���񣨽��鰲װ��3̨������
ִ��ÿ��zookeeper��binĿ¼�µ�zk-installservice.bat

4����װmemcached����
ִ��ÿ��memcached�����memcached-installservice.bat

5����װtomcat����
ִ��ÿ��tomcat�����tomcat_service_install.bat

6������Windows���������棬����������˳����������
������ɺ��������������
http://127.0.0.1/glaf

������������뵽��¼ҳ��
Good Luck��