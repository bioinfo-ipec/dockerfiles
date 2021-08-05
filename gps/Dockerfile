################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="gps methodology dependencies"
LABEL software.version="x"
LABEL about.summary=""
LABEL about.home="https://github.com/homologus/GPS"
LABEL about.documentation="https://github.com/homologus/GPS"
LABEL about.license_file="https://github.com/homologus/GPS"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -c bioconda plink admixture