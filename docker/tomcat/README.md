Docker Tomcat
=============

supervised sshd and Tomcat server with manager apps

`sudo docker build -t oliverlietz/tomcat .`

`sudo docker run -p <host_port>:22 -p <host_port>:8080 -t -name <container_name> oliverlietz/tomcat`
