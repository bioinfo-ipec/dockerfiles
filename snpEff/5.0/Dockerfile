################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="snpEff"
LABEL software.version="5.0"
LABEL about.summary="genetic variant annotation and effect prediction toolbox"
LABEL about.home="https://pcingola.github.io/SnpEff/"
LABEL about.documentation="https://pcingola.github.io/SnpEff/"
LABEL about.license_file="https://pcingola.github.io/SnpEff/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda snpeff=5.0 snpsift tabix
