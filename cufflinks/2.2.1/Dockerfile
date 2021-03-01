################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="cufflinks"
LABEL software.version="2.2.1"
LABEL about.summary="transcriptome assembly and differential expression analysis for RNA-Seq"
LABEL about.home="http://cole-trapnell-lab.github.io/cufflinks/"
LABEL about.documentation="http://cole-trapnell-lab.github.io/cufflinks/"
LABEL about.license_file="http://cole-trapnell-lab.github.io/cufflinks/"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c anaconda libboost

WORKDIR /tmp

RUN wget http://cole-trapnell-lab.github.io/cufflinks/assets/downloads/cufflinks-2.2.1.Linux_x86_64.tar.gz && \ 
      tar -xvf cufflinks-2.2.1.Linux_x86_64.tar.gz && \ 
      rm -rf cufflinks-2.2.1.Linux_x86_64.tar.gz && \ 
      mv ./cufflinks-2.2.1.Linux_x86_64 /usr/local/bin
      
ENV PATH=$PATH:/usr/local/bin/cufflinks-2.2.1.Linux_x86_64