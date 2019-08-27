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

8 配置redis为后台启动(vi命令不会的可以百度,基本就是如何搜索,如何修改,如何保存)
vi /usr/local/redis/etc/redis.conf

9 vi界面下搜索daemonize no 改成daemonize yes

10 
```
