FROM ubuntu
MAINTAINER Ghost <https://github.com/changelit/docker.git>
LABEL apt-source=aliyun 

ENV apt_sources /etc/apt/sources.list

RUN apt-get install -y openssh-server

RUN echo 'deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse' >${apt_sources}
RUN echo 'deb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse' >>${apt_sources}
RUN echo 'deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse' >>${apt_sources}

EXPOSE 22

ENTRYPOINT /usr/sbin/sshd


