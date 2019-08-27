# redis安装目录
/usr/local

# 安装
```
1 下载
wget http://download.redis.io/releases/redis-4.0.8.tar.gz

2 解压
tar -zxvf redis-4.0.8.tar.gz

3 进入文件夹
cd  redis-4.0.8

4 编译
make

5 进入src文件夹
cd src

6 指定安装目录,就是用这个地址就行,乱设置容易忘
make install PREFIX=/usr/local/redis

7 cd到安装目录
cd ../

8 在redis的安装位置创建一个存放配置文件的目录
mkdir /usr/local/redis/etc

9.把配置文件放到刚刚创建的目录中
mv redis.conf /usr/local/redis/etc

10 配置redis为后台启动(vi命令不会的可以百度,基本就是如何搜索,如何修改,如何保存)
vi /usr/local/redis/etc/redis.conf

11 vi界面下搜索daemonize no 改成daemonize yes
/daemonize no
光标移动对应位置按i
删除no
输入yes
esc
:wq
enter

12 将redis加入到开机启动
vi /etc/rc.local 
/usr/local/redis-4.0.8/bin/redis-server /usr/local/redis-4.0.8/redis.conf

//在里面添加内容：/usr/local/redis/bin/redis-server /usr/local/redis/etc/redis.conf


13 启动redis

/usr/local/redis/bin/redis-server /usr/local/redis/etc/redis.conf 

14 启动redis客户端
/usr/local/redis/bin/redis-cli

15 输入ping 收到pong 则连接成功


其他常用命令
pkill redis  //停止redis
 
卸载redis：
rm -rf /usr/local/redis //删除安装目录
 
rm -rf /usr/bin/redis-* //删除所有redis相关命令脚本
```
