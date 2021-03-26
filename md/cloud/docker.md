# docker

## 好处

- 高效利用资源
- 分配、启动速度快
- 运行环境一致
- 容易扩展

## 基本概念

- 镜像
- 容器
- 仓库

## 镜像

### 命令

- pull
- images
- image ls
- image rm
- system df
- build

### Dockerfile

- FROM
- MAINTAINER
- RUN
- COPY
- ADD
- VOLUME
- EXPOSE
- WORKDIR
- CMD
- ENTRYPOINT
- ENV
- ARG
- USER
- HEALTHCHECK

## 容器

### 命令

- run
- container start
- container stop
- attach
- exec
- container rm 
- container prune

### 生命周期

- created：初建状态
- running：运行状态
- stopped：停止状态
- paused： 暂停状态
- deleted：删除状态

## 仓库

- Docker Hub
- Distribution
- harbor

## 主要组件

- docker
- dockerd 
- docker-init
- docker-proxy
- containerd
- containerd-shim 垫片，正在移除
- ctr
- runc

## 底层原理

- namespace 命名空间
  - pid
  - net
  - mnt
  - ipc
  - uts
- cgroups 控制组
  - 资源限制
  - 优先级控制
  - 审计
  - 进程控制
- UnionFS 联合文件系统
- chroot
- 镜像分层

## 网络模式

- none 空网络模式
- bridge 桥接模式
- host 主机网络模式
- container 网络模式

## 配套

### 监控

- cAdvisor

### 工具

- docker compose

### 调度

k8s

## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
