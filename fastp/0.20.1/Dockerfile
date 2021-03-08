################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="fastp"
LABEL software.version="0.20.1"
LABEL about.summary="A FASTQ preprocessor with full features (QC/adapters/trimming/filtering/splitting...)"
LABEL about.home="https://github.com/OpenGene/fastp"
LABEL about.documentation="https://github.com/OpenGene/fastp"
LABEL about.license_file="https://github.com/OpenGene/fastp"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda fastp=0.20.1