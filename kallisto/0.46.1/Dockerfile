################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="kallisto"
LABEL software.version="0.46.1"
LABEL about.summary="quantifies abundances of transcripts from RNA-Seq data, or more generally of target sequences using high-throughput sequencing reads"
LABEL about.home="http://pachterlab.github.io/kallisto"
LABEL about.documentation="http://pachterlab.github.io/kallisto"
LABEL about.license_file="http://pachterlab.github.io/kallisto"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
WORKDIR /tmp

RUN wget https://github.com/pachterlab/kallisto/releases/download/v0.46.1/kallisto_linux-v0.46.1.tar.gz && \
    tar -xf kallisto_linux-v0.46.1.tar.gz && \ 
    rm -rf kallisto_linux-v0.46.1.tar.gz && \
    mv ./kallisto /usr/local/bin

ENV PATH=$PATH:/usr/local/bin/kallisto