FROM ubuntu:22.04

RUN echo "deb http://download.nordugrid.org/repos/7/ubuntu/ jammy-experimental main" >> /etc/apt/sources.list
RUN echo "deb-src http://download.nordugrid.org/repos/7/ubuntu/ jammy-experimental main" >> /etc/apt/sources.list
RUN apt update
RUN apt install -y pip vim nordugrid-arc-client curl wget
RUN pip3 install flask pyyaml
RUN mkdir .knoc
COPY ./client.conf /root/.arc/client.conf