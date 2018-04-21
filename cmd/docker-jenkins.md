```
创建目录并授权
mkdir -p /home/jenkins_home && chmod -R 777 /home/jenkins_home

启动容器
docker run -it -d --restart always --name jenkins -p 8080:8080 -p 50000:50000 -v /home/jenkins_home:/var/jenkins_home jenkins 
```

