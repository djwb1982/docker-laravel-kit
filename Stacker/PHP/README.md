### AgileCMS Docker php-fpm
该容器由网易云容器改动而来。  
1.拉取网易云镜像。  
```
docker pull php:7.0.26-fpm-jessie  
```
2.运行容器。   
```
docker run -d --name php-fpm -p 9000:9000 --net agilecms --ip 172.20.1.9 -v /data/www/agilecms-docker/Stacker/PHP/so/:/var/www/so/ -v /data/www/agilecms-docker/Code/Laravel-Backend/:/usr/share/nginx/html -v /data/www/agilecms-docker/Stacker/PHP/php.ini:/usr/local/etc/php/php.ini <IMAGE ID>  
```
3.进入容器内。  
```
docker exec -it php-fpm /bin/bash   
```