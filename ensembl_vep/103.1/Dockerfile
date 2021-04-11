################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="VEP"
LABEL software.version="103.1"
LABEL about.summary="VEP determines the effect of your variants (SNPs, insertions, deletions, CNVs or structural variants) on genes, transcripts, and protein sequence, as well as regulatory regions"
LABEL about.home="http://www.ensembl.org/info/docs/tools/vep/index.html"
LABEL about.documentation="http://www.ensembl.org/info/docs/tools/vep/index.html"
LABEL about.license_file="http://www.ensembl.org/info/docs/tools/vep/index.html"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
ARG DEBIAN_FRONTEND=noninteractive

RUN conda install -y -c bioconda ensembl-vep=103.1

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