################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="raxml"
LABEL software.version="8.2.12"
LABEL about.summary="program for sequential and parallel Maximum Likelihood based inference of large phylogenetic trees"
LABEL about.home="https://cme.h-its.org/exelixis/web/software/raxml/index.html"
LABEL about.documentation="https://cme.h-its.org/exelixis/web/software/raxml/index.html"
LABEL about.license_file="https://cme.h-its.org/exelixis/web/software/raxml/index.html"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN apt-get update && \ 
    apt-get install -y unzip build-essential

WORKDIR /tmp
RUN wget https://github.com/stamatak/standard-RAxML/archive/v8.2.12.zip && \
    unzip v8.2.12.zip && \ 
    rm -rf v8.2.12.zip && \ 
    mv ./standard-RAxML-8.2.12 /usr/local/bin

WORKDIR /usr/local/bin/standard-RAxML-8.2.12
RUN make -f Makefile.SSE3.gcc

WORKDIR /

ENV PATH=$PATH:/usr/local/bin/standard-RAxML-8.2.12