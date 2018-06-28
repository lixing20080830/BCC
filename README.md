# BCC
百度云服务器安装

首先安装的是jdk，BCC是linux 7 64位，所以需要安装对应的 jdk 7 64位否则会出现 cannot execute binary file 错误

解压命令 tar -zxvf jdk-7u80-linux-x64.tar.gz
移动命令 mv jdk1.7.0_80/ /usr/local/
配置环境变量 vim /etc/profile
![Image text](https://github.com/lixing20080830/BCC/raw/master/images-folder/environment.png)

  
重新加载文件 source /etc/profile
  
JDK安装参考：https://www.cnblogs.com/c-xiaohai/p/6511294.html

我的jkd安装路径：
/usr/local/jdk1.7.0_80

我的Tomcat安装路径：
/usr/local/kencery/tomcat

我的zookeeper安装路径：
/usr/local/zookeeper-3.4.10
查看zookeeper进程--方法：ps -aux | grep 'zookeeper'。系统有返回，说明zookeeper启动。

tomcat安装参考：
https://www.cnblogs.com/hanyinglong/p/5024643.html

我的dubbo-admin安装路径：/usr/local/kencery/tomcat/webapps/dubbo-admin-2.6.0
访问地址：http://106.12.37.42:8888/dubbo-admin-2.6.0/

redis安装命令：
$ wget http://download.redis.io/releases/redis-4.0.10.tar.gz
$ tar xzf redis-4.0.10.tar.gz
$ cd redis-4.0.10
make install PREFIX=/usr/local/redis

注意 mv redis.conf /usr/local/redis/etc换成 mv redis.conf /usr/local/redis/etc/

第一个是启动redis服务器
第二个是启动服务器所需的配置
/usr/local/redis/bin/redis-server /usr/local/redis/etc/redis.conf

客户端连接：
/usr/local/redis/bin/redis-cli 

Redis：密码设置和查看密码
参考资料：https://www.cnblogs.com/suanshun/p/7699084.html

REDIS安装后外网无法访问的问题解决办法：
将其默认的127.0.0.1改为0.0.0.0(代表不做限制)
![Image text](https://github.com/lixing20080830/BCC/raw/master/images-folder/redis.png)


我的rabbitmq安装：
路径是：/usr/local/rabbitmq
首先安装erlang，安装路径：/usr/erlang
参考：https://www.cnblogs.com/mcgrady/p/7614417.html
安装rabbitmq参考：https://blog.csdn.net/qq_34021712/article/details/72567786
我的访问地址：http://106.12.37.42:15672/#/
我的管理员administrator用户名：admin 密码：admin



