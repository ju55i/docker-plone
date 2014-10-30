FROM		ju55i/plone-base:4.3-latest
MAINTAINER	Jussi Talaskivi <jptalask@gmail.com>

WORKDIR	     	/buildout
VOLUME		/buildout/var
ADD		buildout.cfg /buildout/
RUN		buildout
CMD		sed -i "s/REPLACEME/$HOSTNAME/g" parts/instance/etc/zope.conf ; bin/instance console

EXPOSE		8080
