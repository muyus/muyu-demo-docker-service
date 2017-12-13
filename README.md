# 服务配置，services是对container的生产环境搭建，一个service唯一对应一个镜像

1. 初始化 `docker swarm init`
2. 发布服务 `docker stack deploy -c docker-compose.yml muyu-demo-docker-service`

    > 查看服务列表 `docker service ls`	或 `docker service ps muyu-demo-docker-service_web`

3. 扩展服务，修改完配置后，执行 `docker stack deploy -c docker-compose.yml muyu-demo-docker-service` 更新

4. 删除服务 `docker stack rm muyu-demo-docker-service`
5. 删除swarm集群 `docker swarm leave --force`

## 提示: docker --help
