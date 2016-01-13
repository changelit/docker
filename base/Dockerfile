FROM ubuntu
MAINTAINER Ghost <https://github.com/changelit/docker.git>
LABEL apt-source=aliyun 

ENV apt_sources /etc/apt/sources.list

ADD sources.list ${apt_sources}

RUN apt-get update
RUN apt-get install  openssh-server -y

EXPOSE 22

ENTRYPOINT /usr/sbin/sshd


