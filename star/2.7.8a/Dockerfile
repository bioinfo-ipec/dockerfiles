################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="star"
LABEL software.version="2.7.8a"
LABEL about.summary="RNA-seq aligner"
LABEL about.home="https://github.com/alexdobin/STAR"
LABEL about.documentation="https://github.com/alexdobin/STAR"
LABEL about.license_file="https://github.com/alexdobin/STAR"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda star=2.7.8a