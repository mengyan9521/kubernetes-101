# Kubernetes基础总结第1天

## Kubernetes是什么

1. Kubernetes是一种容器编排平台，能够进行自动容器的部署，扩展，和管理
2. Kubernetes是由谷歌以Borg为原本进行开发的，然后通过开源社区进行不断的完善

## Kubernetes能够做什么

1. 可以把容器编排在多个主机上面
2. 进行容器的的健康检查
3. 容器的扩展
4. 服务的发现
5. 已经编排好的容器进行滚动更新
6. 对容器进行监控和Logging
7. 各种权限相关的设置
8. 进行储存的安装

各种各样的组件进行协调和配合，通过这样的方法提供更加优秀的功能

## Kubernetes的主要结构

1. Kubernetes是Master-Worker结构
2. Master对应的是控制平面组件
    1. kube-apiserver：进行API的提供，以及
    2. etcd：类似Kubernetes的操作数据库，集群数据的持久性
    3. kube-scheduler：容器的编排
    4. kube-controller-manager：进行各种资源的控制
3. Worker是对应各个Node，也可以被称为主机
    1. kubelet：容器的启动和监视
    2. kube-proxy：各种资源的转移连接
    3. Container Runtime：各种容器的runtime
