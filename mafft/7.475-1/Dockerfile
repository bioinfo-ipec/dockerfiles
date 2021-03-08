################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="mafft"
LABEL software.version="7.475-1"
LABEL about.summary="multiple alignment program for amino acid or nucleotide sequences"
LABEL about.home="https://mafft.cbrc.jp/alignment/software/"
LABEL about.documentation="https://mafft.cbrc.jp/alignment/software/"
LABEL about.license_file="https://mafft.cbrc.jp/alignment/software/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
WORKDIR /tmp
RUN wget https://mafft.cbrc.jp/alignment/software/mafft_7.475-1_amd64.deb && \
    dpkg -i mafft_7.475-1_amd64.deb && \ 
    rm -rf mafft_7.475-1_amd64.deb