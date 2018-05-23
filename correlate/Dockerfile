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
RUN cd /tmp; wget https://nxlog.co/system/files/products/files/348/nxlog-ce_2.10.2102_ubuntu_bionic_amd64.deb; dpkg -i nxlog-ce_2.10.2102_ubuntu_bionic_amd64.deb
RUN cd /opt; git clone https://github.com/gbarford/net2Host.git
COPY nxlog.conf /etc/nxlog/nxlog.conf
EXPOSE 1514
ENTRYPOINT ["/usr/bin/nxlog"]
CMD ["-f"]
