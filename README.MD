# php_nginx_service_dev

- 在 nginx/conf.d 中创建自己的 conf 文件，添加好conf文件之后需要使用命令`docker-compose -f docker-compose.yaml restart nginx.localdomain`重启nginx服务
- docker-compose.yaml 文件中的 项目目录指向改成自己的即可
- 启动项目：`docker-composer -f docker-compose.yaml up -d`
- 如果遇到项目无法启动的情况，请关掉docker desktop 设置中的 Use gRPC FUSE for file sharing