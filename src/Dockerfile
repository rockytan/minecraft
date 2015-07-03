# VERSION 0.0.1
FROM centos
MAINTAINER Rocky "irockytan@gmail.com"

RUN yum install -y openssh-server sudo  
RUN yum install -y java-1.8.0-openjdk sudo  

RUN useradd rocky
RUN echo "rocky:123.com" | chpasswd  
RUN echo "rocky   ALL=(ALL)       ALL" >> /etc/sudoers

RUN ssh-keygen -t dsa -f /etc/ssh/ssh_host_dsa_key 
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key

RUN mkdir /var/run/sshd  
EXPOSE 22
EXPOSE 25565

CMD ["/usr/sbin/sshd", "-D"]
