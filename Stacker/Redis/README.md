### AgileCMS Docker Redis
该容器由网易云容器改动而来。  
1.拉取网易云镜像。  
```
docker pull docker.io/redis:3.2.11  
```
2.使用dockerfile生成自有镜像。
```  
docker build redis -t agilecms/redis:3.2.11  
```
3.运行容器。   
```
docker run -d -ti -p 6379:6379 --net agilecms --ip 172.20.1.11 -v /data/www/agilecms-docker/Data/Redis:/data --name redis fa69 redis-server  /usr/local/etc/redis/redis.conf  
```
4.进入容器内。  
```
docker exec -it redis /bin/bash
```