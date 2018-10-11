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
 yum install pcre-devel
 ```
 zlib库：
 
 也可以通过yum安装
 ```
 yum install zlib zlib-devel
 ```
