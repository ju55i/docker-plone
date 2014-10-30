FROM       centos:centos7
MAINTAINER Jussi Talaskivi "jptalask@gmail.com"

RUN	   rpm -Uhv http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-2.noarch.rpm
RUN	   yum -y install varnish
ADD	   default.vcl /etc/varnish/default.vcl
CMD	   varnishd -a :6081 -f /etc/varnish/default.vcl -F

EXPOSE	   6081

