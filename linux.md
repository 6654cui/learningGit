# lrzsz
上传文件插件:lrzsz

yum -y install lrzsz 

使用lrzsz

cd 切换到想要保存文件的路径

上传文件执行：
rz 

上传jar包:
rz -E

出现windows的文件选择，选择文件后点击ok，上传 

下载文件执行：

sz finlename

其中filename是想要下载到本地的文件


# vim
基本命令:https://www.jianshu.com/p/8b679b35c9d5


# 防火墙设置:

安装：yum install firewalld

启动： systemctl start firewalld

关闭： systemctl stop firewalld

查看状态： systemctl status firewalld

开机禁用 ： systemctl disable firewalld

开机启用 ： systemctl enable firewalld 

开放5000端口

命令：firewall-cmd --add-port=5000/tcp --zone=public --permanent