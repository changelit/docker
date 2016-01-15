FROM ubuntu
MAINTAINER Ghost <https://github.com/changelit/docker.git>

RUN apt-get install -y curl 

RUN curl -sL https://deb.nodesource.com/setup_0.12 | sudo bash -
RUN apt-get install -y nodejs
RUN npm install pm2 bower -g


