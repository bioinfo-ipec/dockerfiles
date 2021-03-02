################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="bedtools"
LABEL software.version="2.30.0"
LABEL about.summary="a flexible suite of utilities for comparing genomic features"
LABEL about.home="https://bedtools.readthedocs.io/en/latest/"
LABEL about.documentation="https://bedtools.readthedocs.io/en/latest/"
LABEL about.license_file="https://bedtools.readthedocs.io/en/latest/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda bedtools=2.30.0