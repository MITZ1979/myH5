### 1.下载并安装LNMP一键安装包：

```
#### 搭建lnmp集成开发环境

安装LNMP稳定版
如需无人值守安装，请使用 无人值守命令生成工具，或查看无人值守说明教程

wget http://soft.vpser.net/lnmp/lnmp1.5.tar.gz -cO lnmp1.5.tar.gz && tar zxf lnmp1.5.tar.gz && cd lnmp1.5 && ./install.sh lnmp

更多方式
LNMP一键安装包（https://lnmp.org/install.html）

```

### 阿里云服务器搭建lnmp环境

###### 安装 nginx
 #### yum 安装

安装最新nginx源
```
  yum localinstall http://nginx.org/packages/centos/7/noarch/RPMS/nginx-nr-agent-2.0.0-11.el7.ngx.noarch.rpm
```
检查nginx源是否安装成功
```
yum repolist enabled | grep "nginx*"

```
安装nginx
```
yum -y install nginx
启动nginx
service nginx start
设置nginx开机自启动
systemctl enable nginx.service
检查开机自启是否设置成功
systemctl list-dependencies | grep nginx
```
#### 源码安装
 安装make
 ```
 yum -y install gcc automake autoconf libtool make
 ```
 安装g++
 ```
 yum install gcc gcc-c++
 ```
 PCRE库:
 Nginx 需要PCRE(Perl Compatible Regular Expression), 因为Nginx的ReWrite模块和Http核心模块都会使用到PCRE正则表达式语法。其下载地址为http://www.pcre.org/
 也可以通过yum安装
 
 ```
 yum install pcre pcre-devel
 ```
 zlib库：
 zlib库提供了压缩算法，Nginx很多地方都会用到gzip算法。其下载地址为http://www.zlib.net/
 也可以通过yum安装
 ```
 yum install zlib zlib-devel
 ```
OpenSSL:
Nginx中如果服务器提供安全页面，就需要用到OpenSSL库。其下载地址为http://www.openssl.org/
 也可以通过yum安装
 ```
 yum install openssl openssl-devel
 ```
 下载nginx的最新版本
 http://nginx.org/en/download.html
 ```
 wget http://nginx.org/download/nginx-1.5.8.tar.gz
 ```
 解压nginx安装包
 ```
 taar -xzf nginx-1.5.8.tar.gz
 ```
 进入nginx-1.5.8
 ```
 cd nginx-1.5.8
 ```
 执行配置命令[ningx被默认安装在usr/local/nginx中]
 
 ```
 ./configure
 
 ./configure --prefix=/mnt/disk1/nginx--with-http_status_module --with-http_ssl 等等。
 ```
 执行make && make install 安装Nginx
 ```
 make && make install
 ```
 执行nginx-t 检查配置文件是否正确
 ```
 nginx-t
 ```
 进入/usr/local/nginx/sbin目录
 ```
 ./nginx   //启动nginx服务
 ```
 如果发现80端口被占用，可能是ningx服务已经启动。
 ```
 netstat -tunlp|grep 80
 ```
 Nginx相关命令：
 ```
 nginx -h   帮助
 nginx -s stop  立即停止守护进程(TERM信号)
 nginx -s quit  温和的停止守护进程(QUIT信号)
 ```
 
