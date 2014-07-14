FROM       centos:centos7
MAINTAINER Jussi Talaskivi <jptalask@gmail.com>

RUN	   yum -y update
RUN	   yum install -y python-setuptools openssl-devel git tar patch which zlib-devel wget make python-devel bzip2 gcc-c++ libjpeg-devel libxslt-devel readline-devel
RUN	   yum clean all
RUN	   easy_install zc.buildout
RUN	   useradd zope -d /usr/local/zope -s /bin/bash
RUN	   mkdir -p /site ; chown -R zope:zope /site
USER	   zope
WORKDIR    /usr/local/zope
ADD	   buildout.cfg /usr/local/zope/
RUN	   buildout
RUN	   rm -f buildout.cfg
