FROM ubuntu:latest
MAINTAINER navneet.sharma@synechron.com
RUN apt-get -y update 
RUN mkdir /opt/config
ADD config /opt/config
RUN apt-get -y install `cat /opt/config/packages`
ADD code /data/www/
EXPOSE 80
# directly run as a process id:1
CMD /usr/sbin/nginx -g "daemon off;"

