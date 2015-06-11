FROM       python:2.7
MAINTAINER Jussi Talaskivi <jptalask@gmail.com>

RUN	   useradd zope -d /buildout -s /bin/bash -u 65
RUN	   mkdir /buildout ; chown zope /buildout
USER	   zope
WORKDIR    /buildout
ADD	   bootstrap.py /buildout/
ADD	   buildout.cfg /buildout/
RUN	   python bootstrap.py
RUN	   bin/buildout
