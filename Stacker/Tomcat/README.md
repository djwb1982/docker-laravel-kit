### AgileCMS Docker Tomcat
该容器由网易云容器部署，请注意运行容器依据镜像编号启动。  
1.拉取网易云镜像。  
```
docker pull hub.c.163.com/library/tomcat:7.0.81-jre7  
```
2.运行容器。   
```
 docker run --privileged=true -v /vagrant_data/agilecms-docker/code/Tomcat-Backend:/usr/local/tomcat/webapps/www --name=tomcat -p 8888:8080 -d 9539 
```
3.进入容器内。  
```
docker exec -it tomcat /bin/bash
```