################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="subread"
LABEL software.version="2.0.1"
LABEL about.summary="high-performance read alignment, quantification and mutation discovery"
LABEL about.home="http://subread.sourceforge.net"
LABEL about.documentation="http://subread.sourceforge.net"
LABEL about.license_file="http://subread.sourceforge.net"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda subread=2.0.1