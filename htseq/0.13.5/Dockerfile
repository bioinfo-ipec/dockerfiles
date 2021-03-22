################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="HTSeq"
LABEL software.version="0.13.5"
LABEL about.summary="Python library to facilitate processing and analysis of data from high-throughput sequencing (HTS) experiments"
LABEL about.home="https://github.com/htseq/htseq"
LABEL about.documentation="https://github.com/htseq/htseq"
LABEL about.license_file="https://github.com/htseq/htseq"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \ 
    apt-get install -y software-properties-common python3-pip

RUN pip3 install numpy

RUN pip3 install HTSeq==0.13.5