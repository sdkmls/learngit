## Dockerfile

运行dockefile文件

```
docker build -t test .  # . 表示dockerfile这个文件位于当前文件下，构建了一个名叫test的镜像
```

运行镜像

```
docker run test        #运行test这个进行
```

# 各种指令

```
docker search mysql #搜索仓库中mysql相关的镜像
docker pull mysq     #拉取镜像到本地
docker images    #查看现在已经存在的镜像
docker rmi       #删除镜像
docker ps        #列出正在运行的docker容器
docker rm        #删除指点容器
docker logs      #查看容器运行日志
docker stop      #停止容器运行

docker start     #开始运行容器，他只是运行存在的容器
docker run       #创建并运行mysql镜像，他如果检测没有可运行的容器，就会下载目标容器

docker save      #把镜像打包到本地
docker load      #用于加载本地压缩包为docker镜像

docker build     #执行Dockerfile文件
```

