################## BASE IMAGE ######################
FROM continuumio/miniconda3

################## METADATA ######################
LABEL base_image="miniconda3"
LABEL version="latest"
LABEL software="velocyto"
LABEL software.version="0.17.17"
LABEL about.summary="library for the analysis of RNA velocity"
LABEL about.home="http://velocyto.org/velocyto.py/index.html"
LABEL about.documentation="http://velocyto.org/velocyto.py/index.html"
LABEL about.license_file="http://velocyto.org/velocyto.py/index.html"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
ARG DEBIAN_FRONTEND=noninteractive

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

RUN conda config --add channels defaults && \ 
    conda config --add channels bioconda && \ 
    conda config --add channels conda-forge && \
    conda install -y numpy scipy cython numba matplotlib scikit-learn h5py click gcc_linux-64 gxx_linux-64

RUN pip install velocyto

WORKDIR /