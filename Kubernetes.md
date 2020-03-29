# Kubernetes

## 介绍说明

### 发展历史

为什么需要 K8S 的诞生

- 公有云类型说明
	
- 资源管理器对比
- K8S 其优势

### K8S 组件说明

- Borg 组件说明

  ![image-20200329094431516](/Users/jiangshengping/Library/Application Support/typora-user-images/image-20200329094431516.png)

- K8S 结构说明

  - 网络结构
  - 组件结构

### K8S 中的一些关键字解释

#### 



## 基础概念

### Pod 概念

- 自主式 Pod
- 管理器管理的 Pod

	- RS、RC
	- deployment
	- HPA
	- StatefullSet
	- DaemonSet
	- Job，Cronjob

- 服务发现
- Pod 协同

### 网络通讯模式

- 网络通讯模式说明
- 组件通讯模式说明

## Kubernetes 安装

### 系统初始化

### Kubeadm 部署安装

### 常见问题分析

## 资源清单

### K8S 中资源的概念

- 什么是资源
- 名称空间级别的资源
- 集群级别的资源

### 资源清单

- yam 语法格式

### 通过资源清单编写 Pod

### Pod 的生命周期

- initC
- Pod phase
- 容器探针

	- livenessProbe
	- readinessProbe

- Pod hook
- 重启策略

## Pod 控制器

### Pod 控制器说明

- 什么是控制器
- 控制器类型说明

	- ReplicationController 和 ReplicaSet
	- Deployment
	- DaemonSet
	- Job
	- CronJob
	- StatefulSet
	- Horizontal Pod Autoscaling

## 服务发现

### Service 原理

- Service 含义
- Service 常见分类

	- ClusterIP 
	- NodePort  
	- ExternalName  

- Service 实现方式

	- userspace 
	- iptables 
	- ipvs 

### Ingress

- Nginx

	- HTTP 代理访问
	- HTTPS 代理访问
	- 使用 cookie 实现会话关联
	- BasicAuth
	- Nginx 进行重写

## 存储

### configMap 

- 定义概念
- 创建 configMap

	- 使用目录创建
	- 使用文件创建
	- 使用字面值创建

- Pod 中使用 configMap

	- ConfigMap 来替代环境变量
	- ConfigMap 设置命令行参数
	- 通过数据卷插件使用ConfigMap

- configMap 热更新

	- 实现演示
	- 更新触发说明

### Secret 

- 定义概念

	- 概念说明
	- 分类

- Service Account
- Opaque Secret

	- 特殊说明
	- 创建
	- 使用

		- Secret 挂载到 Volume
		- Secret 导出到环境变量中

- kubernetes.io/dockerconfigjson

### volume

- 定义概念

	- 卷的类型

- emptyDir

	- 说明
	- 用途假设
	- 实验演示

- hostPath

	- 说明
	- 用途说明
	- 实验演示

### PV

- 概念解释

	- PV
	- PVC
	- 类型说明

- PV

	- 后端类型
	- PV 访问模式说明
	- 回收策略
	- 状态
	- 实例演示

- PVC

	- PVC 实践演示

## 调度器

### 调度器概念

- 概念
- 调度过程
- 自定义调度器

### 调度亲和性

- nodeAffinity

	- preferredDuringSchedulingIgnoredDuringExecution
	- requiredDuringSchedulingIgnoredDuringExecution

- podAntiAffinity

	- preferredDuringSchedulingIgnoredDuringExecution
	- requiredDuringSchedulingIgnoredDuringExecution

- 亲和性运算符

### 污点

- 污点概念
- Taint

	- 组成
	- 污点的设置、查看和去除

- Tolerations

	- tolerations 设置演示

### 固定节点调度

- PodName 指定调度
- 标签选择器调度

## 集群安全机制

### 机制说明

### 认证

- HTTP Token
- HTTP Base
- HTTPS 

### 鉴权

- AlwaysDeny
- AlwaysAllow
- ABAC
- Webbook
- RBAC

	- RBAC
	- Role and ClusterRole
	- RoleBinding and ClusterRoleBinding
	- Resources
	- to Subjects
	- 创建一个系统用户管理 k8s dev 名称空间：重要实验

### 准入控制

## HELM

### HELM 概念

- HELM 概念说明
- 组将构成
- HELM 部署
- HELM 自定义

### HELM 部署实例

- HELM 部署 dashboard
- metrics-server

	- HPA 演示
	- 资源限制

		- Pod
		- 名称空间

- Prometheus
- EFK

## 运维

### Kubeadm 源码修改

### Kubernetes 高可用构建

*XMind: ZEN - Trial Version*