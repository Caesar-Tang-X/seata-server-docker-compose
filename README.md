# Seata-Server 2.0.0 Docker Compose YML File


## 简介
    docker 一键启动 Seata-Server 2.0.0 容器的 docker-compose.yml 配置，采用 【无注册中心，DB存储】


## 镜像环境：
	mysql:8.0
    seata-server:2.0.0


## 导入镜像：
	docker load -i 镜像包


## 启动命令：
	docker-compose up -d


## 安装及生成数据路径：
    ├── seata-server 
        ├── images                      镜像文件文件目录
        ├── db                          数据库容器挂载目录
            ├── conf                        配置文件目录
            ├── data                        数据目录
            └── log                         日志目录
        ├── seata-server                应用容器挂载目录
            └── resources                   配置文件目录
        ├── docker-compose.yml          docker-compose.yml
        └── README.md                   README.md


## 隐私信息配置：
	1. 修改 MySQL 账号密码, 文件路径：docker-compose.yml
    2. 修改应用配置文件, 文件路径：seata-server/resources/application.yml
