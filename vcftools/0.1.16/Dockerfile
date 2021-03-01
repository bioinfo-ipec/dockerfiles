################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="sratoolkit"
LABEL software.version="0.1.16"
LABEL about.summary="works with VCF files"
LABEL about.home="https://vcftools.github.io/"
LABEL about.documentation="https://vcftools.github.io/"
LABEL about.license_file="https://vcftools.github.io/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda vcftools