################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="fastqc"
LABEL software.version="0.11.92"
LABEL about.summary="A quality control tool for high throughput sequence data"
LABEL about.home="https://www.bioinformatics.babraham.ac.uk/projects/fastqc/"
LABEL about.documentation="https://www.bioinformatics.babraham.ac.uk/projects/fastqc/"
LABEL about.license_file="https://www.bioinformatics.babraham.ac.uk/projects/fastqc/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda fastqc=0.11.9