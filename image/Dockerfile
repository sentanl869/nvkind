FROM kindest/node:v1.33.1

ARG NVIDIA_TOOLKIT=nvidia-container-toolkit_1.17.8_deb_amd64.tar.gz

COPY ${NVIDIA_TOOLKIT} /tmp/

RUN \
    sed -i 's#http://deb\.debian\.org#https://mirrors.tuna.tsinghua.edu.cn#g' /etc/apt/sources.list.d/debian.sources && \
    cd /tmp && \
    tar -zxvf ${NVIDIA_TOOLKIT} && \
    cd release-v1.17.8-stable/packages/ubuntu18.04/amd64 && \
    dpkg -i *.deb && \
    rm -rf /tmp/*
