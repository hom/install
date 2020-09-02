# Maridb

`mariadb`是`mysql`的开源替代版本，使用方式和`mysql`是一样的

## 查看已安装的版本

`centos`查看已安装的版本

```bash
rpm -qa | grep mariadb
```

删除已安装的版本

```bash
rpm -e --nodeps mariadb-*
```

## 安装

1. 新建`Mariadb.repo`源文件

```bash
vim /etc/yum.repos.d/Mariadb.repo
```

写入内容

```bash
name = MariaDB
baseurl = http://yum.mariadb.org/10.4/centos7-amd64
gpgkey=https://yum.mariadb.org/RPM-GPG-KEY-MariaDB
gpgcheck=1
```

2. 安装

```bash
yum -y install MariaDB-server MariaDB-client
```

## 启动

```bash
# 启动
systemctl start mariadb

# 设置开机启动
systemctl enable mariadb

# 重启
systemctl restart mariadb

# 查看运行状态
systemctl status mariadb

# 取消开机启动
systemctl disable mariadb
```
