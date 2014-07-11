from       fedora
MAINTAINER Jussi Talaskivi <jptalask@gmail.com>

#run	yum -y update
run	yum install -y python-pip openssl-devel tar patch which zlib-devel wget make python-devel bzip2 gcc-c++ libjpeg-devel libxslt-devel readline-devel
run	yum clean all
run	mkdir -p /usr/local/zope/ ; useradd zope -d /usr/local/zope -s /bin/bash ; chown -R zope:zope /usr/local/zope
run	mkdir -p /site ; chown -R zope:zope /site
run	pip install zc.buildout
