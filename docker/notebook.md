```bash
docker stop `docker ps -a -q`    // stop all container, then images could be del.
docker rm `docker ps -a -q`     // remove all container
docker images
docker rmi image_id
docker rmi $(docker images | grep "^<none>" | awk "{print $3}")
docker rmi $(docker images -q)  // remove all images

docker exec -it 966832a8f582 /bin/bash    //进容器后台
docker run -t -i image_name /bin/bash     //根据镜像启动容器，进入bash
-p 5000:5000               //绑定特定端口号
-v /webapp training/webapp // -v 挂载 本机文件夹到容器

# 把一个宿主机上的目录挂载到镜像里。
docker run -it -v /home/dock/Downloads:/usr/Downloads ubuntu64 /bin/bash

docker start xxxx


# 网络管理
docker run -P：随机分配端口号
docker run -p 5000:5000：绑定特定端口号（主机的所有网络接口的5000端口均绑定容器的5000端口）
docker run -p 127.0.0.1:5000:5000：绑定主机的特定接口的端口号
docker run -d -p 127.0.0.1:5000:5000/udp training/webapp python app.py：绑定udp端口号
docker port<CONTAINER_ID> 5000：查看容器的5000端口对应本地机器的IP和端口号




docker attach     //命令-登录一个已经在执行的容器 (link is external)
docker build      //命令-建立一个新的image (link is external)
docker commit     //命令-提交一个新的image (link is external)
docker cp     //命令-将容器中的文件拷贝到主机上 (link is external)
docker daemon     //命令-docker运行可指定项详解 (link is external)
docker diff     //命令-较一个容器不同版本提交的文件差异 (link is external)
docker events     //命令-获取sever中的实时事件 (link is external)
docker export     //命令-导出一个容器 (link is external)
docker history     //命令-显示一个image的历史 (link is external)
docker images     //命令-列出image (link is external)
docker import     //命令-导入已有的image (link is external)
docker info     //命令-展示docker的信息 (link is external)
docker inspect     //命令-显示更底层的容器或image信息 (link is external)
docker kill     //命令-杀死docker进程 (link is external)
docker load     //命令-加载image (link is external)
docker login     //命令-登录docker注册服务器 (link is external)
docker logs     //命令-获取容器的日志 (link is external)
docker pause     //命令-暂停容器中的所有进程 (link is external)
docker port     //命令 端口转发 (link is external)
docker ps     //命令-列出所有容器 (link is external)
docker pull     //命令-从远端拉取一个image (link is external)
docker push     //命令-推送image到注册服务器 (link is external)
docker restart     //命令-重启一个容器或多个容器 (link is external)
docker rmi     //命令-删除image (link is external)
docker rm     //命令-删除一个或多个容器 (link is external)
docker run     //命令-运行一个新的容器 (link is external)
docker save     //命令-打包image (link is external)
docker search     //命令-搜索images (link is external)
docker start     //命令-启动一个容器 (link is external)
docker stop     //命令-停止一个容器 (link is external)
docker tag     //命令-为image打标签 (link is external)
docker top     //命令-显示容器中的进程 (link is external)
docker unpause     //命令-取消暂停所有的进程 (link is external)
docker version     //命令-显示版本信息 (link is external)
docker wait     //命令-阻塞容器运行
```
