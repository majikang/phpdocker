# phpdocker
## 介绍
自己个人使用的docker开发环境，适用laravel。
## 常用命令
#### 运行 NGINX 和 MySQL:
```bash
docker-compose up -d  nginx mysql
```

#### 进入 Workspace 容器
```bash
docker-compose exec workspace bash
```
退出容器, `exit`.

#### 列出正在运行的容器
```bash
docker ps
```
你也可以使用以下命令查看某项目的容器

#### 查看容器
```bash
docker-compose ps
```

#### 查看容器IP地址等信息
```bash
docker inspect {容器id} | grep IPAddress
```

#### 关闭所有容器
```bash
docker-compose stop
```

#### 停止某个容器:

```bash
docker-compose stop {容器名称}
```

#### 删除所有容器
```bash
docker-compose down
```

#### 建立/重建容器

如果你改变了`dockerfile`，运行这个命令让所有修改更改生效:

```bash
docker-compose build
```
指定哪个容器重建(而不是重建所有的容器):

```bash
docker-compose build {container-name}
```

重建整个容器，可以需要使用 `--no-cache` 选项  (`docker-compose build --no-cache {container-name}`).