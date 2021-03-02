################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="picard"
LABEL software.version="2.25.0"
LABEL about.summary="A set of command line tools (in Java) for manipulating high-throughput sequencing (HTS) data and formats such as SAM/BAM/CRAM and VCF."
LABEL about.home="https://github.com/broadinstitute/picard"
LABEL about.documentation="https://github.com/broadinstitute/picard"
LABEL about.license_file="https://github.com/broadinstitute/picard"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda picard=2.25.0