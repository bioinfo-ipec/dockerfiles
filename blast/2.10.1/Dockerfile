################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="blast"
LABEL software.version="2.10.1"
LABEL about.summary="finds regions of similarity between biological sequences. The program compares nucleotide or protein sequences to sequence databases and calculates the statistical significance."
LABEL about.home="https://blast.ncbi.nlm.nih.gov/Blast.cgi"
LABEL about.documentation="https://blast.ncbi.nlm.nih.gov/Blast.cgi"
LABEL about.license_file="https://blast.ncbi.nlm.nih.gov/Blast.cgi"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda blast