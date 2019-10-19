### Django应用docker化

> 本项目把Django应用和Nginx放在一个容器中

> 容器中运行着两个个进程: nginx, uwsgi

> 上述两个个进程由supervisor管理

> supervisor提供web管理界面 http://ip:9001

### 编译
```
docker build . -t django-in-docker:dev
```

### 启动
```
docker run -p 8001:8001 -p 9001:9001 \
-d \
-t django-in-docker:dev
```
