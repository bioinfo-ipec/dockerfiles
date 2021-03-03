################## BASE IMAGE ######################
FROM ubuntu:20.04

################## METADATA ######################
LABEL base_image="ubuntu:20.04"
LABEL version="latest"
LABEL software="samtools"
LABEL software.version="1.11"
LABEL about.summary="manipulates next-generation sequencing data"
LABEL about.home="https://github.com/samtools/samtools"
LABEL about.documentation="https://github.com/samtools/samtools"
LABEL about.license_file="https://github.com/samtools/samtools"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN apt-get update && \ 
    apt-get install -y autoconf automake make gcc perl zlib1g-dev libbz2-dev liblzma-dev libcurl4-gnutls-dev libssl-dev libncurses5-dev wget unzip

WORKDIR /tmp
RUN wget -O /tmp/htslib.zip https://github.com/samtools/htslib/archive/1.11.zip && \
    unzip htslib.zip && \ 
    rm -rf htslib.zip
WORKDIR /tmp/htslib-1.11
RUN autoreconf -i && \
    ./configure && \
    make && \
    make install

WORKDIR /tmp
RUN wget -O /tmp/samtools.zip https://github.com/samtools/samtools/archive/1.11.zip && \
    unzip samtools.zip && \ 
    rm -rf samtools.zip
WORKDIR /tmp/samtools-1.11
RUN autoheader && \
    autoconf -Wno-syntax && \
    autoreconf && \
    ./configure && \
    make && \
    make install

WORKDIR /tmp
RUN wget -O /tmp/bcftools.zip https://github.com/samtools/bcftools/archive/1.11.zip && \
    unzip bcftools.zip && \ 
    rm -rf bcftools.zip
WORKDIR /tmp/bcftools-1.11
RUN autoheader && \
    autoconf && \
    autoreconf && \
    ./configure && \
    make && \
    make install

WORKDIR /