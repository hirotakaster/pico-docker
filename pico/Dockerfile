FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -y sudo git cmake pkg-config python3 \
               gcc-arm-none-eabi libnewlib-arm-none-eabi vim \
               language-pack-ja-base language-pack-ja

ENV USER=ubuntu
ENV HOME=/home/${USER}
ENV PASSWORD=ubuntu
ENV SHELL=/bin/bash
ENV UID=1000
ENV GID=1000

RUN groupadd -g ${GID} ${USER}
RUN useradd -m --uid ${UID} --gid ${GID} ${USER}
RUN gpasswd -a ${USER} sudo
RUN echo ${USER}:${PASSWORD} | chpasswd

USER ${USERNAME}
WORKDIR ${HOME}
CMD ["bash"]

RUN locale-gen ja_JP.UTF-8
ENV LANG ja_JP.UTF-8

