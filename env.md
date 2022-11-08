# Linux环境搭建指南


1.下载镜像文件(.iso)
http://mirrors.aliyun.com/ubuntu-releases/
2.使用VMware安装	
3.配置镜像源
https://blog.csdn.net/weixin_42426340/article/details/107750109?spm=1001.2014.3001.5501
仅作参考，需要替换为对应版本的源，否则可能出现安装软件时出现异常情况
4.配置静态IP
通过图形界面配置，如果配置完成无法访问网络，可以试试配置dns为8.8.8.8
5.设置samba
https://blog.csdn.net/qq_41004932/article/details/117486105
sudo vim /etc/samba/smb.conf

配置文件：
[share]
path = /home/hw
available = yes
valid users = hw
read only = no
browsable = yes
public = yes
writable = yes

重启samba服务：
sudo service smbd restart

6.配置ssh
https://blog.csdn.net/chao_shine/article/details/106966854

7.安装必备的工具
1) git
sudo apt install git
https://zhuanlan.zhihu.com/p/557738982

git push -u origin main

2) fzf
3) bat
4) delta
	see sbin/delta




问题解决：
1.键盘删除键、上下键无法使用：
https://blog.csdn.net/qq_43686329/article/details/120430069
2.时间不正确
https://blog.csdn.net/u013066730/article/details/124152798
3.设置不锁屏
https://jingyan.baidu.com/article/0202781174d49a5acc9ce5b3.html
