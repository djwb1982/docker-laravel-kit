### AgileCMS Docker Mysql
该容器由网易云容器部署，请注意运行容器依据镜像编号启动。   
1.拉取网易云镜像。  
```
docker pull mysql:5.5.58  
```
2.运行容器。   
```
docker run --name mysql --net agilecms --ip 172.20.1.10 -p 3306:3306 -v /data/www/agilecms-docker/Data/Mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -d af2c --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci 
```
3.进入容器内。  
```
docker exec -it mysql /bin/bash
```