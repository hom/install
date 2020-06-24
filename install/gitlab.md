# Gitlab

### 安装方式

- docker
- script
- packages

### docker

1. 下载镜像

   ```bash
   docker pull gitlab/gitlab-ce:latest
   ```

   

2. 添加存储位置和端口映射

   ```bash
   docker run \
       --publish 443:443 --publish 80:80 --publish 22:22 \
       --name gitlab-ce \
       --volume /data/gitlab/config:/etc/gitlab \
       --volume /data/gitlab/logs:/var/log/gitlab \
       --volume /data/gitlab/data:/var/opt/gitlab \
       gitlab/gitlab-ce
   ```

   

3. 查看启动状态

   ```bash
   docker ps -a
   ```

   如果启动成功则会显示

   ```bash
   CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                    PORTS                                                                  NAMES
   6c8596bf420c        gitlab/gitlab-ce    "/assets/wrapper"   19 minutes ago      Up 19 minutes (healthy)   0.0.0.0:20022->22/tcp, 0.0.0.0:20080->80/tcp, 0.0.0.0:20443->443/tcp   gitlab-ce
   ```

   

