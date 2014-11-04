FROM       centos:centos7
MAINTAINER Jussi Talaskivi <jptalask@gmail.com>

RUN	   yum -y update
RUN	   yum install -y python-setuptools openssl-devel git tar patch which zlib-devel wget make python-devel bzip2 gcc-c++ libjpeg-devel libxslt-devel readline-devel
RUN	   yum clean all
RUN	   useradd zope -d /buildout -s /bin/bash -u 65
USER	   zope
WORKDIR    /buildout
ADD	   bootstrap.py /buildout/
ADD	   buildout.cfg /buildout/
RUN	   python bootstrap.py
RUN	   bin/buildout
