################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="bwa"
LABEL software.version="0.7.17"
LABEL about.summary="maps low-divergent sequences against a large reference genome"
LABEL about.home="http://bio-bwa.sourceforge.net"
LABEL about.documentation="http://bio-bwa.sourceforge.net"
LABEL about.license_file="http://bio-bwa.sourceforge.net"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda bwa=0.7.17