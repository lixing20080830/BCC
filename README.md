# BCC
百度云服务器安装

首先安装的是jdk，BCC是linux 7 64位，所以需要安装对应的 jdk 7 64位否则会出现 cannot execute binary file 错误

解压命令 tar -zxvf jdk-7u80-linux-x64.tar.gz
移动命令 mv jdk1.7.0_80/ /usr/local/
配置环境变量 vim /etc/profile
　　export JAVA_HOME=/usr/local/jdk1.7.0_80
　　export JRE_HOME=/usr/local/jdk1.7.0_80/jre 
　　export PATH=$PATH:/usr/local/jdk1.7.0_80/bin 
　　export CLASSPATH=./:/usr/local/jdk1.7.0_80/lib:/usr/local/jdk1.7.0_80/jre/lib
  
  重新加载文件 source /etc/profile
  
  
  参考：https://www.cnblogs.com/c-xiaohai/p/6511294.html




