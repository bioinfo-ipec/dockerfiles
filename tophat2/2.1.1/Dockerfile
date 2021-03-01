################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="tophat2"
LABEL software.version="2.1.1"
LABEL about.summary="a spliced read mapper for RNA-Seq"
LABEL about.home="https://github.com/DaehwanKimLab/tophat"
LABEL about.documentation="https://github.com/DaehwanKimLab/tophat"
LABEL about.license_file="https://github.com/DaehwanKimLab/tophat"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda tophat