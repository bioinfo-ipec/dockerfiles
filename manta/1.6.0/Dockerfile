################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="manta"
LABEL software.version="1.6.0"
LABEL about.summary="Structural variant and indel caller for mapped sequencing data"
LABEL about.home="https://github.com/Illumina/manta"
LABEL about.documentation="https://github.com/Illumina/manta"
LABEL about.license_file="https://github.com/Illumina/manta"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda manta=1.6.0