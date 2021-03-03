################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="hisat2"
LABEL software.version="2.2.1"
LABEL about.summary="graph-based alignment of next generation sequencing reads to a population of genomes"
LABEL about.home="https://github.com/DaehwanKimLab/hisat2"
LABEL about.documentation="https://github.com/DaehwanKimLab/hisat2"
LABEL about.license_file="https://github.com/DaehwanKimLab/hisat2"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN apt-get update && \ 
    apt-get install -y unzip

WORKDIR /tmp

RUN wget -O hisat2.zip https://cloud.biohpc.swmed.edu/index.php/s/oTtGWbWjaxsQ2Ho/download && \
    unzip hisat2.zip && \ 
    rm -rf hisat2.zip && \ 
    mv ./hisat2-2.2.1 /usr/local/bin

ENV PATH=$PATH:/usr/local/bin/hisat2-2.2.1