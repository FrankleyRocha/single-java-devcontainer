FROM ubuntu:24.04
SHELL ["/bin/bash", "-ic"]

RUN apt update

#pacotes essenciais
RUN apt install -y \
    vim \
    curl \
    git \
    sudo \
    zip unzip

ARG USERNAME=ubuntu

RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME

RUN curl -s "https://get.sdkman.io" | bash

RUN sdk install java 21.0.6-tem
RUN sdk install maven
