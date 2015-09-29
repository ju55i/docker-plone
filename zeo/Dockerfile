FROM		ju55i/plone-base:5-latest
MAINTAINER 	Jussi Talaskivi <jptalask@gmail.com>

# Everything is run as a zope user
WORKDIR	     	/buildout
ADD		buildout.cfg /buildout/
RUN		bin/buildout
CMD		sed -i "s/REPLACEME/$HOSTNAME/g" parts/zeoserver/etc/zeo.conf ; bin/zeoserver fg

EXPOSE		8100
