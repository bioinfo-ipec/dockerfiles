################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="bowtie"
LABEL software.version="1.3.0"
LABEL about.summary="an ultrafast memory-efficient short read aligner"
LABEL about.home="https://github.com/BenLangmead/bowtie"
LABEL about.documentation="https://github.com/BenLangmead/bowtie"
LABEL about.license_file="https://github.com/BenLangmead/bowtie"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda bowtie