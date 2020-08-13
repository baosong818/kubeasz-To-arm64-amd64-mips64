# ![install](install.png)

```
声明：
所有文件均来自互联网，本人只是大自然的搬运工
涉及到公司的代码已删除
如有冒犯请通知本人，及时删除
```

```
部署方式
1、使用Dockerfile基于debian生成个镜像，网络太差，上传不到hub去
2、自行安装ansible，反正大概其都是Dockerfile里面的命令，你apt、yum了就行了，然后拷贝ansible目录到相应地方
3、install/clean你懂，理论是一键部署，我测试的结果
4、上图为amd64、arm64混构
```

```
以下为兼容arm64/amd64的镜像，测试通过，misp64的需要去龙芯那里下载
#FROM kubernetesui/dashboard:v2.0.3
#FROM jessestuart/tiller:v2.16.7
#FROM rancher/hyperkube:v1.14.8-rancher2

#FROM carlosedp/kube-state-metrics:v1.9.6
#FROM prom/node-exporter:v1.0.1
#FROM rancher/hyperkube:v1.16.12-rancher1
#FROM carlosedp/prometheus-config-reloader:v0.39.0
#FROM carlosedp/configmap-reload:latest 
#FROM carlosedp/prometheus-operator:v0.39.0
#FROM jettech/kube-webhook-certgen:v1.3.0
#FROM raspbernetes/ghostunnel:v1.5.2
#FROM prom/alertmanager:v0.21.0
#FROM prom/prometheus:v2.19.2

#k8s v1.15.12
#FROM kubesphere/kube-apiserver:v1.15.12
#FROM kubesphere/kube-proxy:v1.15.12
#FROM kubesphere/kube-controller-manager:v1.15.12
#FROM kubesphere/kube-scheduler:v1.15.12
#FROM coredns/coredns:1.3.1
#FROM kontenapharos/etcd:3.3.10
#FROM kubesphere/pause:3.1
#FROM calico/kube-controllers:v3.9.6
#FROM calico/pod2daemon-flexvol:v3.9.6
#FROM calico/node:v3.9.6
#FROM calico/cni:v3.9.6
#FROM calico/kube-controllers:v3.13.5
#FROM calico/pod2daemon-flexvol:v3.13.5
#FROM calico/node:v3.13.5
#FROM calico/cni:v3.13.5

#k8s v1.17.9
#FROM kubesphere/kube-apiserver:v1.17.9
#FROM kubesphere/kube-proxy:v1.17.9
#FROM kubesphere/kube-controller-manager:v1.17.9
#FROM kubesphere/kube-scheduler:v1.17.9
#FROM kubesphere/pause:3.1
#FROM coredns/coredns:1.6.5
#FROM mirrorgcrio/etcd-amd64:3.4.3-0
#FROM mirrorgcrio/etcd-arm64:3.4.3-0
#@FROM --platform=$BUILDPLATFORM node:alpine AS build
#@ARG TARGETARCH
#@FROM mirrorgcrio/etcd-${TARGETARCH}:3.4.3-0
#FROM calico/cni:v3.15.1
#FROM calico/pod2daemon-flexvol:v3.15.1
#FROM calico/node:v3.15.1
#FROM calico/kube-controllers:v3.15.1

#k8s v1.18.6
#FROM kubesphere/kube-apiserver:v1.18.6
#FROM kubesphere/kube-proxy:v1.18.6
#FROM kubesphere/kube-controller-manager:v1.18.6
#FROM kubesphere/kube-scheduler:v1.18.6
#FROM kubesphere/pause:3.2
#FROM coredns/coredns:1.6.7
#FROM --platform=$BUILDPLATFORM node:alpine AS build
#ARG TARGETARCH
#FROM mirrorgcrio/etcd-${TARGETARCH}:3.4.3-0
```
