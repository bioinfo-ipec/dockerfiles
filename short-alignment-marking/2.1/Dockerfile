################## BASE IMAGE ######################
FROM continuumio/miniconda3

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="short alignment marking"
LABEL software.version="2.1"
LABEL about.summary="Tool to mark short alignments in a bam file."
LABEL about.home="https://github.com/nygenome/nygc-short-alignment-marking"
LABEL about.documentation="https://github.com/nygenome/nygc-short-alignment-marking"
LABEL about.license_file="https://github.com/nygenome/nygc-short-alignment-marking"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
WORKDIR /tmp
RUN git clone https://github.com/nygenome/nygc-short-alignment-marking.git

ENV LD_LIBRARY_PATH=/tmp/nygc-short-alignment-marking/lib:$LD_LIBRARY_PATH
ENV PATH=$PATH:/tmp/nygc-short-alignment-marking

WORKDIR /