################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="strelka"
LABEL software.version="2.9.10"
LABEL about.summary="Strelka calls somatic and germline small variants from mapped sequencing reads"
LABEL about.home="https://github.com/Illumina/strelka"
LABEL about.documentation="https://github.com/Illumina/strelka"
LABEL about.license_file="https://github.com/Illumina/strelka"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -c bioconda strelka=2.9.10