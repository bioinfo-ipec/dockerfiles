################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="rsem"
LABEL software.version="1.3.3"
LABEL about.summary="estimates gene and isoform expression levels from RNA-Seq data"
LABEL about.home="https://deweylab.github.io/RSEM/"
LABEL about.documentation="https://deweylab.github.io/RSEM/"
LABEL about.license_file="https://deweylab.github.io/RSEM/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda rsem=1.3.3