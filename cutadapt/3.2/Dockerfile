################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="cutadapt"
LABEL software.version="3.2"
LABEL about.summary="finds and removes adapter sequences, primers, poly-A tails and other types of unwanted sequence from your high-throughput sequencing reads"
LABEL about.home="https://cutadapt.readthedocs.io/en/stable/"
LABEL about.documentation="https://cutadapt.readthedocs.io/en/stable/"
LABEL about.license_file="https://cutadapt.readthedocs.io/en/stable/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda cutadapt=3.2