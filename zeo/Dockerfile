FROM		ju55i/plonebase:4.3-latest
MAINTAINER 	Jussi Talaskivi <jptalask@gmail.com>

# Everything is run as a zope user
WORKDIR	     	/usr/local/zope
VOLUME		/site
ADD		buildout.cfg /usr/local/zope/
RUN		buildout
CMD		bin/zeoserver fg

EXPOSE		8100
