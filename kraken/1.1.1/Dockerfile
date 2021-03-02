################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="kraken"
LABEL software.version="1.1.1"
LABEL about.summary="an system for assigning taxonomic labels to short DNA sequences, usually obtained through metagenomic studies."
LABEL about.home="http://ccb.jhu.edu/software/kraken/"
LABEL about.documentation="http://ccb.jhu.edu/software/kraken/"
LABEL about.license_file="http://ccb.jhu.edu/software/kraken/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda kraken=1.1.1