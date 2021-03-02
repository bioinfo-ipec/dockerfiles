################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="stringtie"
LABEL software.version="2.1.4"
LABEL about.summary=" fast and highly efficient assembler of RNA-Seq alignments into potential transcripts"
LABEL about.home="https://github.com/gpertea/stringtie"
LABEL about.documentation="https://github.com/gpertea/stringtie"
LABEL about.license_file="https://github.com/gpertea/stringtie"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda stringtie=2.1.4