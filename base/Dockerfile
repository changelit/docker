FROM ubuntu
MAINTAINER Ghost <https://github.com/changelit/docker.git>
LABEL apt-source=aliyun 

ENV apt_sources /etc/apt/sources.list

ADD sources.list ${apt_sources}

RUN apt-get install -y openssh-server

EXPOSE 22

ENTRYPOINT /usr/sbin/sshd


