FROM       centos:centos7
MAINTAINER Jussi Talaskivi <jptalask@gmail.com>

RUN	   yum -y update
RUN	   yum install -y python-setuptools openssl-devel git tar patch which zlib-devel wget make python-devel bzip2 gcc-c++ libjpeg-devel libxslt-devel readline-devel
RUN	   yum clean all
RUN	   easy_install zc.buildout
WORKDIR    /buildout
ADD	   buildout.cfg /buildout/
RUN	   buildout
