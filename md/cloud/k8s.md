# K8s

## 作用

- 调度
- 亲和、反亲和
- 健康检查
- 容错
- 可扩展性
- 网络
- 服务发现
- 滚动升级
- HPA

## 重要组件

### 控制面板

#### kube-apiserver

- 认证
- 授权
- 访问控制
- 服务发现

#### kube-scheduler

- 监听Pod

#### kube-controller-manager

- 副本创建
- 滚动升级

### Node节点

- kube-proxy
- kubelet

### 其他

- etcd
- core dns
- ingress controller
- dashboard

## 集群工具

- kind
- minikube
- kubeadm
- rancher2

## Pod

### metadata
### spec
### status

### 内置namespace

- default
- kube-system
- kube-public
- kube-node-lease

### Probe

- livenessProbe
- readinessProbe
- startupProbe

### Hook

- PostStart
- PreStop

## Kind

- Pod
- Deployment
- Service
  - ClusterIP
  - NodePort
  - LoadBalancer
  - ExternalName
- StatefulSet
- ConfigMap
- Secret
- PersistentVolume
- PersistentVolumeClaim
- StorageClass
- DaemonSet 
- LimitRange
- ResourceQuota 
- PriorityClass
- CronJob
- Job
- APIService
- CustomResourceDefinition

## Volume

- configMap 
- secret
- downwardAPI
- emptyDir
- hostPath



## Helm

- Chart
- Config
- Release


## 问题 

### 日志

- fluentd
- elasticsearch
- kibana


### 监控

- cAdvisor
- heapster（废弃）
- metrics-server
- kube-state-metrics
- node-exporter
- prometheus
- grafana 

## 资源保护

- Requests 
- Limits 
- QoS级别
  - BestEffort
  - Burstable 
  - Guranteed
