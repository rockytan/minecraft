#Raneto Dockerfile
#Version 0.1

FROM centos:latest
MAINTAINER Rocky "irockytan@gmail.com"

RUN yum install -y npm git sudo
WORKDIR /app

RUN git clone https://github.com/gilbitron/Raneto.git && \
    cd Raneto && npm install

WORKDIR /app/Raneto

EXPOSE 3000
EXPOSE 22

CMD ["/usr/bin/npm","start"]
