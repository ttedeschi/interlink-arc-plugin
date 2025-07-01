FROM ubuntu:22.04

RUN apt update
RUN apt install -y pip vim curl wget
RUN wget -q http://download.nordugrid.org/DEB-GPG-KEY-nordugrid-7.asc -O- | apt-key add -
RUN echo "deb http://download.nordugrid.org/repos/7/ubuntu/ jammy main" >> /etc/apt/sources.list
RUN echo "deb-src http://download.nordugrid.org/repos/7/ubuntu/ jammy main" >> /etc/apt/sources.list
RUN apt update
RUN apt install -y nordugrid-arc-client
RUN pip3 install flask pyyaml
RUN mkdir .knoc
COPY ./client.conf /root/.arc/client.conf
COPY ./handles.py /handles.py
COPY ./SidecarConfig.yaml /SidecarConfig.yaml
