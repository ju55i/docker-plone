FROM       python:2.7
MAINTAINER Jussi Talaskivi <jptalask@gmail.com>

RUN	   useradd -m -d /buildout zope
USER	   zope
WORKDIR    /buildout
RUN	   mkdir -p /buildout/.buildout/eggs /buildout/.buildout/downloads /buildout/.buildout/extends
ADD	   default.cfg /buildout/.buildout/default.cfg
ADD	   bootstrap.py /buildout/
ADD	   buildout.cfg /buildout/
RUN	   python bootstrap.py
RUN	   bin/buildout
