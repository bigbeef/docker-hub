docker build --build-arg jenkins_version=2.222.3 -t winfed/jenkins:2.222.3-arm64v8 .

docker push winfed/jenkins:2.222.3-arm64v8
