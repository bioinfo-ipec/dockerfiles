################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="kraken"
LABEL software.version="1.1.1"
LABEL about.summary="an system for assigning taxonomic labels to short DNA sequences, usually obtained through metagenomic studies."
LABEL about.home="http://ccb.jhu.edu/software/kraken/"
LABEL about.documentation="http://ccb.jhu.edu/software/kraken/"
LABEL about.license_file="http://ccb.jhu.edu/software/kraken/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN apt-get update && \ 
    apt-get install -y unzip build-essential

WORKDIR /tmp
RUN wget https://github.com/DerrickWood/kraken/archive/v1.1.1.zip && \
    unzip v1.1.1.zip && \ 
    rm -rf v1.1.1.zip

WORKDIR /tmp/kraken-1.1.1
RUN ./install_kraken.sh /usr/local/bin/kraken

ENV PATH=$PATH:/usr/local/bin/kraken