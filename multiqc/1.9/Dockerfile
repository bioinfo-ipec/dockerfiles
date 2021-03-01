################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="multiqc"
LABEL software.version="1.9"
LABEL about.summary="create aggregate bioinformatics analysis reports across many samples and tools"
LABEL about.home="https://github.com/ewels/MultiQC"
LABEL about.documentation="https://github.com/ewels/MultiQC"
LABEL about.license_file="https://github.com/ewels/MultiQC"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda multiqc