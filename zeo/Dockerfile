FROM		ju55i/plone-base:4.3-latest
MAINTAINER 	Jussi Talaskivi <jptalask@gmail.com>

# Everything is run as a zope user
WORKDIR	     	/buildout
VOLUME		/buildout/var/blobstorage
VOLUME		/buildout/var/filestorage
ADD		buildout.cfg /buildout/
RUN		buildout
CMD		sed -i "s/REPLACEME/$HOSTNAME/g" parts/zeoserver/etc/zeo.conf ; bin/zeoserver fg

EXPOSE		8100
