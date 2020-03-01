FROM alpine:3.11.3
MAINTAINER oldiy <oldiy@163.com>

WORKDIR /
ENV NPS_VERSION 0.26.3

RUN set -x && \
	wget --no-check-certificate https://github.com/ehang-io/nps/releases/download/v${NPS_VERSION}/linux_amd64_server.tar.gz && \ 
	tar xzf linux_amd64_server.tar.gz && \
	mkdir -p /opt/nps && \
	cd /opt/nps && \
	mkdir \npsconf && \
	cp conf/* npsconf/ && \
	cd .. && \
	rm -rf *.tar.gz

ADD start.sh /opt/nps/npsconf/start.sh

RUN chmod +x /opt/nps/npsconf/start.sh

VOLUME /opt/nps/conf

CMD /opt/nps/npsconf/start.sh
