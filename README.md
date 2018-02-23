### AgileCMS
本系统由三个部分构成：Code,Data,Stacker。  
Stacker：为docker镜像配置和生成容器。  
Data:为容器映射出来的数据库路径。  
Code:为系统代码部分。    
主体实现场景是以单独系统部署为主，未考虑编排功能。  
关于docker加速：  
推荐使用daocloud.io。

创建容器网络：
```
 docker network create -o "com.docker.network.bridge.name"="agilecms" --subnet 172.20.0.0/16 rhcms
```

