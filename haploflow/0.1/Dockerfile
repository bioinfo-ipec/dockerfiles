################## BASE IMAGE ######################
FROM ubuntu:20.04

################## METADATA ######################
LABEL base_image="ubuntu:20.04"
LABEL version="latest"
LABEL software="haploflow"
LABEL software.version="0.1"
LABEL about.summary="strain-aware viral genome assembler for short read sequence data"
LABEL about.home="https://github.com/hzi-bifo/Haploflow"
LABEL about.documentation="https://github.com/hzi-bifo/Haploflow"
LABEL about.license_file="https://github.com/hzi-bifo/Haploflow"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \ 
    apt-get install -y unzip build-essential libboost-all-dev cmake git

WORKDIR /usr/local/bin

RUN git clone https://github.com/hzi-bifo/Haploflow.git && \
    cd Haploflow && \
    mkdir build && \
    cd build && \
    cmake .. && \
    make

ENV PATH=$PATH:/usr/local/bin/Haploflow/build