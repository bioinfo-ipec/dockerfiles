################## BASE IMAGE ######################
FROM ubuntu:20.04

################## METADATA ######################
LABEL base_image="ubuntu:20.04"
LABEL version="latest"
LABEL software="multiqc"
LABEL software.version="1.10"
LABEL about.summary="create aggregate bioinformatics analysis reports across many samples and tools"
LABEL about.home="https://github.com/ewels/MultiQC"
LABEL about.documentation="https://github.com/ewels/MultiQC"
LABEL about.license_file="https://github.com/ewels/MultiQC"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \ 
    apt-get install -y software-properties-common python3-pip

RUN pip3 install multiqc==1.10