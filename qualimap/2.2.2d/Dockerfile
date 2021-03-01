################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="qualimap"
LABEL software.version="2.2.2d"
LABEL about.summary="facilitates the quality control of alignment sequencing data and its derivatives like feature counts"
LABEL about.home="http://qualimap.conesalab.org"
LABEL about.documentation="http://qualimap.conesalab.org"
LABEL about.license_file="http://qualimap.conesalab.org"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda qualimap