# Docker Tomcat
FROM stackbrew/debian:7.2
MAINTAINER Oliver Lietz <info@oliverlietz.de>

RUN apt-get update
RUN apt-get -y upgrade
RUN apt-get -y install supervisor openssh-server openjdk-7-jre-headless tomcat7 tomcat7-admin

RUN mkdir -p /var/run/sshd
RUN mkdir -p /var/log/supervisor

RUN echo "root:root" | chpasswd

ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 22 8080

ENTRYPOINT ["/usr/bin/supervisord"]
