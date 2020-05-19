1. 安装`yum-utils`
```bash
yum install -y yum-utils
```

2. 添加`yum`源。

```bash
vim /etc/yum.repos.d/nginx.repo
```

内容如下：

```bash
[nginx-stable]
name=nginx stable repo
baseurl=http://nginx.org/packages/centos/$releasever/$basearch/
gpgcheck=1
enabled=1
gpgkey=https://nginx.org/keys/nginx_signing.key
module_hotfixes=true

[nginx-mainline]
name=nginx mainline repo
baseurl=http://nginx.org/packages/mainline/centos/$releasever/$basearch/
gpgcheck=1
enabled=0
gpgkey=https://nginx.org/keys/nginx_signing.key
module_hotfixes=true
```
3. 执行安装命令
```bash
yum install -y nginx
```
4. 查看`nginx`版本
```bash
#查看nginx版本
nginx -v
#查看编译参数
nginx -V
```
5. 查看安装目录
```bash
rpm -ql nginx
```
6. 查看配置文件
```bash
# 用于日志切割
/etc/logrotate.d/nginx
```
