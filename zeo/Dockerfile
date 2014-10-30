FROM		ju55i/plonebase:4.3-latest
MAINTAINER 	Jussi Talaskivi <jptalask@gmail.com>

# Everything is run as a zope user
WORKDIR	     	/buildout
VOLUME		/buildout/var
ADD		buildout.cfg /buildout/
RUN		buildout
CMD		sed -i "s/REPLACEME/$HOSTNAME/g" parts/zeoserver/etc/zeo.conf ; bin/zeoserver fg

EXPOSE		8100
