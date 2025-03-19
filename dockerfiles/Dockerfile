FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl git gcc g++ make

RUN apt-get update && apt-get install -y zlib1g-dev libncurses-dev liblzma-dev libbz2-dev libcurl4-gnutls-dev libcrypto++-dev libdeflate-dev

RUN git clone --recursive https://github.com/samtools/htslib.git && \
    git clone --recursive https://github.com/samtools/samtools.git && \
    cd /root/samtools/ && make && make install

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=samtools
