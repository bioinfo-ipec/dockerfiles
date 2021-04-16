################## BASE IMAGE ######################
FROM continuumio/miniconda3

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="VarScan"
LABEL software.version="2.4.4"
LABEL about.summary="Variant calling and somatic mutation/CNV detection for next-generation sequencing data"
LABEL about.home="http://varscan.sourceforge.net"
LABEL about.documentation="http://varscan.sourceforge.net"
LABEL about.license_file="http://varscan.sourceforge.net"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -c bioconda varscan=2.4.4

