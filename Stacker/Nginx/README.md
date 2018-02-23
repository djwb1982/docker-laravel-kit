### AgileCMS Docker Nginx
该容器由网易云容器改动而来。  
1.拉取网易云镜像。  
```
docker pull docker.io/nginx:1.13  
```
4.3.运行容器。   
```
docker run -d --name nginx --net agilecms --ip 172.20.1.8 -p 80:80 -v /data/www/agilecms-docker/Stacker/Nginx/nginx.conf:/etc/nginx/nginx.conf -v /data/www/agilecms-docker/Code/Laravel-Backend/:/usr/share/nginx/html 4610  
```
4.进入容器内。  
```
docker exec -it nginx /bin/bash
```