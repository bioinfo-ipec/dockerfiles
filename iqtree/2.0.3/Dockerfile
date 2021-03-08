################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="iqtree"
LABEL software.version="2.0.3"
LABEL about.summary="efficient phylogenomic software by maximum likelihood"
LABEL about.home="https://github.com/Cibiv/IQ-TREE"
LABEL about.documentation="https://github.com/Cibiv/IQ-TREE"
LABEL about.license_file="https://github.com/Cibiv/IQ-TREE"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda iqtree=2.0.3