# docker-hub
由于所需kubernetes镜像被墙，需要优雅的拉取镜像

For Example
```
docker pull winfed/kube-proxy:v1.12.1
docker pull winfed/kube-apiserver:v1.12.1
docker pull winfed/kube-scheduler:v1.12.1
docker pull winfed/kube-controller-manager:v1.12.1
docker pull winfed/etcd:3.2.24
docker pull winfed/coredns:1.2.2
docker pull winfed/pause:3.1
docker pull winfed/flannel:v0.10.0-amd64


docker tag winfed/kube-proxy:v1.12.1 k8s.gcr.io/kube-proxy:v1.12.1
docker tag winfed/kube-apiserver:v1.12.1 k8s.gcr.io/kube-apiserver:v1.12.1
docker tag winfed/kube-scheduler:v1.12.1 k8s.gcr.io/kube-scheduler:v1.12.1
docker tag winfed/kube-controller-manager:v1.12.1 k8s.gcr.io/kube-controller-manager:v1.12.1
docker tag winfed/etcd:3.2.24 k8s.gcr.io/etcd:3.2.24
docker tag winfed/coredns:1.2.2 k8s.gcr.io/coredns:1.2.2
docker tag winfed/pause:3.1 k8s.gcr.io/pause:3.1
docker tag winfed/flannel:v0.10.0-amd64 quay.io/coreos/flannel:v0.10.0-amd64

docker rmi winfed/kube-proxy:v1.12.1
docker rmi winfed/kube-apiserver:v1.12.1
docker rmi winfed/kube-scheduler:v1.12.1
docker rmi winfed/kube-controller-manager:v1.12.1
docker rmi winfed/etcd:3.2.24
docker rmi winfed/coredns:1.2.2
docker rmi winfed/pause:3.1
docker rmi winfed/flannel:v0.10.0-amd64
```
