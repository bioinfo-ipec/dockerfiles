################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="gcta"
LABEL software.version="1.93.2beta"
LABEL about.summary="GCTA (Genome-wide Complex Trait Analysis) was initially designed to estimate the proportion of phenotypic variance explained by all genome-wide SNPs for complex traits (i.e., the GREML method). It has been subsequently extended for many other analyses to better understand the genetic architecture of complex traits. GCTA currently supports the following analyses"
LABEL about.home="https://cnsgenomics.com/software/gcta"
LABEL about.documentation="https://cnsgenomics.com/software/gcta"
LABEL about.license_file="https://cnsgenomics.com/software/gcta"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN apt-get update && \ 
    apt-get install -y unzip

WORKDIR /tmp
RUN wget -O gcta.zip https://cnsgenomics.com/software/gcta/bin/gcta_1.93.2beta.zip && \
    unzip gcta.zip && \ 
    rm -rf gcta.zip && \ 
    mv ./gcta_1.93.2beta /usr/local/bin

ENV PATH=$PATH:/usr/local/bin/gcta_1.93.2beta