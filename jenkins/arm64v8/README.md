## Dockerfile
```
https://github.com/bigbeef/docker-hub/tree/master/jenkins/arm64v8
```

## build
```
docker build --build-arg jenkins_version=2.222.3 -t winfed/jenkins:2.222.3-arm64v8 .
```

## push 
```
docker push winfed/jenkins:2.222.3-arm64v8
```
