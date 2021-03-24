################## BASE IMAGE ######################
FROM continuumio/miniconda3

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="trim-galore"
LABEL software.version="0.6.6"
LABEL about.summary="automates quality and adapter trimming as well as quality control"
LABEL about.home="https://github.com/FelixKrueger/TrimGalore"
LABEL about.documentation="https://github.com/FelixKrueger/TrimGalore"
LABEL about.license_file="https://github.com/FelixKrueger/TrimGalore"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \ 
    apt-get install -y curl pigz

RUN pip3 install --upgrade cutadapt==3.0

WORKDIR /tmp
RUN curl -fsSL https://github.com/FelixKrueger/TrimGalore/archive/0.6.6.tar.gz -o trim_galore.tar.gz && \
    tar xvzf trim_galore.tar.gz && \ 
    rm -rf trim_galore.tar.gz && \ 
    mv ./TrimGalore-0.6.6 /usr/local/bin

ENV PATH=$PATH:/usr/local/bin/TrimGalore-0.6.6