################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="trimmomatic"
LABEL software.version="0.39"
LABEL about.summary="a flexible read trimming tool for Illumina NGS data"
LABEL about.home="http://www.usadellab.org/cms/?page=trimmomatic"
LABEL about.documentation="http://www.usadellab.org/cms/?page=trimmomatic"
LABEL about.license_file="http://www.usadellab.org/cms/?page=trimmomatic"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda trimmomatic=0.39