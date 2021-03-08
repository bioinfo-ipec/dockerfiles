################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="vcflib"
LABEL software.version="1.0.0"
LABEL about.summary="Command-line tools for manipulating VCF files"
LABEL about.home="https://github.com/vcflib/vcflib"
LABEL about.documentation="https://github.com/vcflib/vcflib"
LABEL about.license_file="https://github.com/vcflib/vcflib"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda vcflib