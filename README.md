# BCC
百度云服务器安装一条龙<br/>

JDK
-------
首先安装的是jdk，BCC是linux 7 64位，所以需要安装对应的 jdk 7 64位否则会出现 cannot execute binary file 错误<br/>

解压命令 tar -zxvf jdk-7u80-linux-x64.tar.gz<br>
移动命令 mv jdk1.7.0_80/ /usr/local/<br>
配置环境变量 vim /etc/profile<br>
/etc/profile文件中修改环境变量，在这里修改的内容是对所有用户起作用的。<br>
![Image text](https://github.com/lixing20080830/BCC/raw/master/images-folder/environment.png)<br>

重新加载文件 source /etc/profile<br>
  
JDK安装参考：https://www.cnblogs.com/c-xiaohai/p/6511294.html<br>

我的jkd安装路径：<br>
/usr/local/jdk1.7.0_80<br/><br>

tomcat
-------
我的Tomcat安装路径：<br>
/usr/local/kencery/tomcat<br>

tomcat安装参考：
https://www.cnblogs.com/hanyinglong/p/5024643.html<br>

zookeeper
-------
我的zookeeper安装路径：<br>
/usr/local/zookeeper-3.4.10<br>
查看zookeeper进程--方法：ps -aux | grep 'zookeeper'。系统有返回，说明zookeeper启动。<br>

dubbo-admin
-------
我的dubbo-admin安装路径：/usr/local/kencery/tomcat/webapps/dubbo-admin-2.6.0<br/>
访问地址：http://106.12.37.42:8888/dubbo-admin-2.6.0/<br/>

redis
-------
redis安装步骤：<br>
$ wget http://download.redis.io/releases/redis-4.0.10.tar.gz<br>
$ tar xzf redis-4.0.10.tar.gz<br>
$ cd redis-4.0.10<br>
make install PREFIX=/usr/local/redis<br>

注意 mv redis.conf /usr/local/redis/etc换成 mv redis.conf /usr/local/redis/etc/<br>

第一个是启动redis服务器
第二个是启动服务器所需的配置
/usr/local/redis/bin/redis-server /usr/local/redis/etc/redis.conf<br>

客户端连接：
/usr/local/redis/bin/redis-cli<br> 

我的密码：lixing<br>
Redis：密码设置和查看密码
参考资料：https://www.cnblogs.com/suanshun/p/7699084.html

REDIS安装后外网无法访问的问题解决办法：<br>
将其默认的127.0.0.1改为0.0.0.0(代表不做限制)<br>
![Image text](https://github.com/lixing20080830/BCC/raw/master/images-folder/redis.png)<br>

rabbitmq
-------
我的rabbitmq安装：
路径是：/usr/local/rabbitmq<br>
首先安装erlang，安装路径：/usr/erlang<br>
参考：https://www.cnblogs.com/mcgrady/p/7614417.html<br>
安装rabbitmq参考：https://blog.csdn.net/qq_34021712/article/details/72567786<br>
我的访问地址：http://106.12.37.42:15672/#/<br>
我的管理员administrator用户名：admin 密码：admin<br>

### activemq
我的activemq安装路径：<br>
/usr/local/activemq/<br>
在/usr/local/activemq/bin 目录下执行./activemq start<br>
因为之前安装了rabbitmq，出现端口冲突<br>
解决方法参考：<br>
https://blog.csdn.net/pansanday/article/details/78024811<br>

访问地址：http://106.12.37.42:8161/admin/ 用户名：admin 密码：admin<br>

