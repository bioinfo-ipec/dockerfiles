################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="AfterQC"
LABEL software.version="0.9.7"
LABEL about.summary="automatic Filtering, Trimming, Error Removing and Quality Control for fastq data"
LABEL about.home="https://github.com/OpenGene/AfterQC"
LABEL about.documentation="https://github.com/OpenGene/AfterQC"
LABEL about.license_file="https://github.com/OpenGene/AfterQC"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda afterqc
