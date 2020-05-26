# Yarn:hammer:

1. 在 CentOS、Fedora 和 RHEL上
```bash
$ curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
```

2. 如果没有安装`Node.js`，需要先安装

```bash
curl --silent --location https://rpm.nodesource.com/setup_12.x | sudo bash -
```

3. 接下來你可以很簡單的使用以下指令安裝

```bash
$ sudo yum install -y yarn
## 或是 ##
$ sudo dnf install -y yarn
```

4. 執行命令來测试 Yarn 是否安裝

```bash
$ yarn --version
```
