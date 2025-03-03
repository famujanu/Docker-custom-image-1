==========================================================================================================================================
FROM centos:latest
LABEL version="v1.0"
LABEL description="The Image from nginx web server"

RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

RUN yum -y install java
RUN yum -y install telnet
RUN yum -y install vim
RUN yum -y install curl

WORKDIR /var/www/html
COPY index.html ./

EXPOSE 80
CMD ["nginx","-g","daemon off;"]


ENV 
root@test1-centos docker]# cat  Dockerfile
FROM centos:latest
LABEL version="v1.0"
LABEL description="The Image from nginx web server"

RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

ENV PORT="80"
ENV ENVIROMENT="development"


RUN yum -y install java
RUN yum -y install telnet
RUN yum -y install vim
RUN yum -y install curl

WORKDIR /var/www/html
COPY index.html ./

EXPOSE $PORT
CMD ["nginx","-g","daemon off;"]


USER
====================================================
docker image build -t mywebserver10 .
docker image build -t mywebserver10 .


docker image build -t mywebserver10 .
[+] Building 105.2s (15/15) FINISHED                                                                                             docker:default
 => [internal] load build definition from Dockerfile                                                                                       0.0s
 => => transferring dockerfile: 624B                                                                                                       0.0s
 => [internal] load metadata for docker.io/library/centos:latest                                                                           2.0s
 => [internal] load .dockerignore                                                                                                          0.0s
 => => transferring context: 2B                                                                                                            0.0s
 => [ 1/10] FROM docker.io/library/centos:latest@sha256:a27fd8080b517143cbbbab9dfb7c8571c40d67d534bbdee55bd6c473f432b177                   0.0s
 => [internal] load build context                                                                                                          0.1s
 => => transferring context: 134B                                                                                                          0.0s
 => CACHED [ 2/10] RUN cd /etc/yum.repos.d/                                                                                                0.0s
 => CACHED [ 3/10] RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*                                                       0.0s
 => CACHED [ 4/10] RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*            0.0s
 => [ 5/10] RUN yum -y install java                                                                                                       77.0s
 => [ 6/10] RUN yum -y install telnet                                                                                                      4.1s
 => [ 7/10] RUN yum -y install vim                                                                                                        12.1s
 => [ 8/10] RUN yum -y install curl                                                                                                        6.4s
 => [ 9/10] WORKDIR /var/www/html                                                                                                          0.1s
 => [10/10] COPY index.html ./                                                                                                             0.0s
 => exporting to image                                                                                                                     3.2s
 => => exporting layers                                                                                                                    3.2s
 => => writing image sha256:e296129fad0a5410a07ed678f95193045d68bbc4876481e3d1cabb8d3d162f0c                                               0.0s
 => => naming to docker.io/library/                                                                                            0.0s
[root@test1-centos docker]#

[root@test1-centos docker]# docker image ls
REPOSITORY             TAG       IMAGE ID       CREATED          SIZE
mywebserver10          latest    e296129fad0a   55 seconds ago   556MB
docker image inspect mywebserver10          

 "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "PORT=80",
                "ENVIROMENT=development"
            ],


docker container run -d --name mycustomNginx10 -P mywebserver10
394629f5e13290fba4f0193b267583eba9a67dc7db1c510378928b235fcd7f42
docker container inspect mycustomNginx10

Config": {
            "Hostname": "394629f5e132",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "80/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "PORT=80",
                "ENVIROMENT=development"


docker container run -d --name mymycustomNginx11 -P --env ENVIROMENT="Production" mywebserver10
docker container run -d --name mymycustomNginx11 -P --env ENVIROMENT="Production" mywebserver10
0d15c426a043f7a5fdee95f2685c6b21f85906001e505c1467c2eec5ad5af303


docker container inspect mymycustomNginx11


 "Config": {
            "Hostname": "0d15c426a043",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "80/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "ENVIROMENT=Production",
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "PORT=80"
            ],
====================================
cat mywebserver9
FROM centos:latest
LABEL version="v1.0"
LABEL description="The Image from nginx web server"

RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

RUN yum -y install java
RUN yum -y install telnet
RUN yum -y install vim
RUN yum -y install curl

WORKDIR /var/www/html
COPY index.html ./

EXPOSE 80
CMD ["nginx","-g","daemon off;"]
[root@test1-centos docker]#
===============================================================================================

docker image build -t mywebserver11 .
[+] Building 1.9s (15/15) FINISHED                                                                                               docker:default
 => [internal] load build definition from Dockerfile                                                                                       0.0s
 => => transferring dockerfile: 624B                                                                                                       0.0s
 => [internal] load metadata for docker.io/library/centos:latest                                                                           1.7s
 => [internal] load .dockerignore                                                                                                          0.0s
 => => transferring context: 2B                                                                                                            0.0s
 => [ 1/10] FROM docker.io/library/centos:latest@sha256:a27fd8080b517143cbbbab9dfb7c8571c40d67d534bbdee55bd6c473f432b177                   0.0s
 => [internal] load build context                                                                                                          0.0s
 => => transferring context: 91B                                                                                                           0.0s
 => CACHED [ 2/10] RUN cd /etc/yum.repos.d/                                                                                                0.0s
 => CACHED [ 3/10] RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*                                                       0.0s
 => CACHED [ 4/10] RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*            0.0s
 => CACHED [ 5/10] RUN yum -y install java                                                                                                 0.0s
 => CACHED [ 6/10] RUN yum -y install telnet                                                                                               0.0s
 => CACHED [ 7/10] RUN yum -y install vim                                                                                                  0.0s
 => CACHED [ 8/10] RUN yum -y install curl                                                                                                 0.0s
 => CACHED [ 9/10] WORKDIR /var/www/html                                                                                                   0.0s
 => CACHED [10/10] COPY index.html ./                                                                                                      0.0s
 => exporting to image                                                                                                                     0.0s
 => => exporting layers                                                                                                                    0.0s
 => => writing image sha256:e296129fad0a5410a07ed678f95193045d68bbc4876481e3d1cabb8d3d162f0c                                               0.0s
 => => naming to docker.io/library/mywebserver11                                                                                           0.0s
[root@test1-centos docker]#
=================================

 cat Dockerfile
FROM centos:latest
LABEL version="v1.0"
LABEL description="The Image from nginx web server"

RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

ENV PORT="80"
ENV ENVIROMENT="development"

RUN useradd -ms /bin/bash devopsuser
USER devopsuser
WORKDIR /home/devopsuser





EXPOSE $PORT
CMD ["nginx","-g","daemon off;"]


==========================================================

docker image build -t mywebserver12 .
[+] Building 0.9s (10/10) FINISHED                                                                                               docker:default
 => [internal] load build definition from Dockerfile                                                                                       0.0s
 => => transferring dockerfile: 566B                                                                                                       0.0s
 => [internal] load metadata for docker.io/library/centos:latest                                                                           0.7s
 => [internal] load .dockerignore                                                                                                          0.0s
 => => transferring context: 2B                                                                                                            0.0s
 => [1/6] FROM docker.io/library/centos:latest@sha256:a27fd8080b517143cbbbab9dfb7c8571c40d67d534bbdee55bd6c473f432b177                     0.0s
 => CACHED [2/6] RUN cd /etc/yum.repos.d/                                                                                                  0.0s
 => CACHED [3/6] RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*                                                         0.0s
 => CACHED [4/6] RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*              0.0s
 => CACHED [5/6] RUN useradd -ms /bin/bash devopsuser                                                                                      0.0s
 => CACHED [6/6] WORKDIR /home/devopsuser                                                                                                  0.0s
 => exporting to image                                                                                                                     0.0s
 => => exporting layers                                                                                                                    0.0s
 => => writing image sha256:fbfa62408dae601a20d3dffaa03eca7e571b8456ce41cdb85b91d7d4392d94a3                                               0.0s
 => => naming to docker.io/library/mywebserver12                                                                                           0.0s
[root@test1-centos docker]#
