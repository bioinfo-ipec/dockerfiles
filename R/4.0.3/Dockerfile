################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="R"
LABEL software.version="4.0.3"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c conda-forge r-base=4.0.3 r-docopt=0.7.1
