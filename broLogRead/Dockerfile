FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y wget 
RUN apt-get install -y redis-tools
RUN apt-get install -y python3-redis
RUN apt-get install -y libapr1
RUN apt-get install -y libdbi1
RUN apt-get install -y libperl5.26
RUN apt-get install -y libcap2
RUN apt-get install -y libssl1.0.0
RUN apt-get install -y vim
RUN apt-get install -y python3-elasticsearch
RUN apt-get install -y git
RUN apt-get install -y supervisor
RUN cd /opt; git clone https://github.com/gbarford/net2Host.git
RUN mkdir /var/log/net2Host
RUN mkdir /var/lib/net2Host
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
CMD ["/usr/bin/supervisord"]
