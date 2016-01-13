FROM ubuntu
MAINTAINER Ghost <https://github.com/changelit/docker.git>
LABEL apt-source=aliyun 

ENV apt_sources /etc/apt/sources.list

ADD sources.list ${apt_sources}

RUN apt-get update
RUN apt-get install  openssh-server -y
RUN mkdir /var/run/sshd

#Add password to root user
RUN echo 'root:root' |chpasswd

#Allow root user to login 
RUN sed -ri 's/^PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]


