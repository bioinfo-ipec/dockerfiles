################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="qualimap"
LABEL software.version="2.2.2d"
LABEL about.summary="facilitates the quality control of alignment sequencing data and its derivatives like feature counts"
LABEL about.home="http://qualimap.conesalab.org"
LABEL about.documentation="http://qualimap.conesalab.org"
LABEL about.license_file="http://qualimap.conesalab.org"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN apt-get update && \ 
    apt-get install -y unzip libxrender1 libxtst6 libxi6 libxext6

WORKDIR /tmp

RUN wget https://bitbucket.org/kokonech/qualimap/downloads/qualimap_v2.2.1.zip && \
    unzip qualimap_v2.2.1.zip && \ 
    rm -rf hisat2.zip && \
    mv ./qualimap_v2.2.1 /usr/local/bin

RUN conda install -y -c anaconda openjdk
RUN conda install -y -c conda-forge r-base=4.0.3

RUN R -e "install.packages(c('BiocManager', 'optparse', 'XML'), dependencies=TRUE, repos='http://cran.rstudio.com/')"
RUN R -e "BiocManager::install(c('NOISeq', 'Repitools'))"

ENV PATH=$PATH:/usr/local/bin/qualimap_v2.2.1