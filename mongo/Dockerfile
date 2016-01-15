FROM ubuntu
MAINTAINER Ghost <https://github.com/changelit/docker.git>

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
RUN echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
RUN sudo apt-get update
RUN sudo apt-get install -y mongodb-org=3.0.1 mongodb-org-server=3.0.1 mongodb-org-shell=3.0.1 mongodb-org-mongos=3.0.1 mongodb-org-tools=3.0.1

RUN  echo 'export LANG=C' >>/etc/profile
RUN  sed -i 's/^bind/#&/' /etc/mongod.conf