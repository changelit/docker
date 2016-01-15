FROM ubuntu
MAINTAINER Ghost <https://github.com/changelit/docker.git>

RUN apt-get install  openssh-server -y
RUN mkdir /var/run/sshd

#Add password to root user
RUN echo 'root:root' |chpasswd

#Allow root user to login 
RUN sed -ri 's/^PermitRootLogin\s+.*/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -ri 's/UsePAM yes/#UsePAM yes/g' /etc/ssh/sshd_config

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]
