```
docker run \
    --detach \
    --publish 443:443 \
    --publish 80:80 \
    --publish 22:22 \
    --name gitlab \
    --restart unless-stopped \
    --volume /home/gitlab/etc:/etc/gitlab \
    --volume /home/gitlab/log:/var/log/gitlab \
    --volume /home/gitlab/data:/var/opt/gitlab \
    beginor/gitlab-ce:10.4.1-ce.0



docker run \
    --detach \
    --publish 443:443 \
    --publish 80:80 \
    --publish 22:22 \
    --name gitlab \
    --restart always \
    --volume /home/gitlab/etc:/etc/gitlab \
    --volume /home/gitlab/log:/var/log/gitlab \
    --volume /home/gitlab/data:/var/opt/gitlab \
    beginor/gitlab-ce:10.4.1-ce.0

获得权限
sudo chmod -R 777 /home/gitlab/

docker container ls

docker container ls -a

docker container rm id

清除所有处于终止状态的容器
docker container prune

创建ssh key
ssh-keygen -t rsa -C "jenkins@sishuguojixuefu.com"

重新配置
docker exec gitlab gitlab-ctl reconfigure
重启
docker exec gitlab gitlab-ctl restart
备份
docker exec gitlab gitlab-rake gitlab:backup:create

恢复
docker exec gitlab gitlab-rake gitlab:backup:restore BACKUP=1393513186
```

