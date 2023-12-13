## Dockerfile
```
https://github.com/bigbeef/docker-hub/tree/master/jenkins/arm64v8
```

## build & push
```
# debian
docker build --build-arg jenkins_version=2.414.3 -t winfed/jenkins:2.414.3-arm64v8 .
docker push winfed/jenkins:2.414.3-arm64v8

# centos
docker build --build-arg jenkins_version=2.414.3 -f Dockerfile-CentOS -t winfed/jenkins:2.414.3-centos-arm64v8 .
docker push winfed/jenkins:2.414.3-centos-arm64v8
```
