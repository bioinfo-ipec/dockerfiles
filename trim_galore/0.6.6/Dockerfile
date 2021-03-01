################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="trim-galore"
LABEL software.version="0.6.6"
LABEL about.summary="automates quality and adapter trimming as well as quality control"
LABEL about.home="https://github.com/FelixKrueger/TrimGalore"
LABEL about.documentation="https://github.com/FelixKrueger/TrimGalore"
LABEL about.license_file="https://github.com/FelixKrueger/TrimGalore"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda trim-galore