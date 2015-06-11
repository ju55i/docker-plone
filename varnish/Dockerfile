FROM       centos:centos7
MAINTAINER Jussi Talaskivi "jptalask@gmail.com"

RUN	   yum -y install epel-release
RUN	   yum -y install varnish
ADD	   default.vcl /etc/varnish/default.vcl
CMD	   varnishd -a :6081 -f /etc/varnish/default.vcl -F

EXPOSE	   6081

