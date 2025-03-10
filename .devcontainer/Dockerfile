FROM ubuntu:24.04
SHELL ["/bin/bash", "-ic"]

RUN apt update

#pacotes essenciais
RUN apt install -y \
    curl \
    git \
    sudo \
    zip unzip

RUN echo ubuntu ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/ubuntu \
    && chmod 0440 /etc/sudoers.d/ubuntu

USER ubuntu

RUN curl -s "https://get.sdkman.io" | bash

RUN sdk install java 21.0.6-tem
RUN sdk install maven
