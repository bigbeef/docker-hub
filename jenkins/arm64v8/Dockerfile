FROM adoptopenjdk/openjdk11:jdk-11.0.21_9

RUN  apt-get install -y curl && rm -rf /var/lib/apt/lists/*

ARG user=jenkins
ARG group=jenkins
ARG uid=1000
ARG gid=1000
ARG jenkins_url=https://mirrors.huaweicloud.com/jenkins/war-stable
ARG jenkins_version=2.401.3

ENV JENKINS_HOME=/var/jenkins_home JENKINS_VERSION=${jenkins_version}

WORKDIR ${JENKINS_HOME}

RUN mkdir -p /usr/share/jenkins;

RUN set -eux; \
    groupadd -g ${gid} ${group}; \
    useradd -u ${uid} -g ${gid} ${user}; \
    curl -s ${jenkins_url}/${JENKINS_VERSION}/jenkins.war -o /usr/share/jenkins/jenkins.war ;\
    chown -R ${user}:${group} ${JENKINS_HOME};

USER ${user}

EXPOSE 8080

VOLUME [ "${JENKINS_HOME}" ]

ENTRYPOINT [ "java", "-jar", "/usr/share/jenkins/jenkins.war", "--httpPort=8080"]
