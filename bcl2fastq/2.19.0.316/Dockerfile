################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="bcl2fastq"
LABEL software.version="2.20.0"
LABEL about.summary="Conversion Software both demultiplexes data and converts BCL files generated by Illumina sequencing systems to standard FASTQ file formats for downstream analysis"
LABEL about.home="https://support.illumina.com/sequencing/sequencing_software/bcl2fastq-conversion-software.html"
LABEL about.documentation="https://support.illumina.com/sequencing/sequencing_software/bcl2fastq-conversion-software.html"
LABEL about.license_file="https://support.illumina.com/sequencing/sequencing_software/bcl2fastq-conversion-software.html"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -c dranew bcl2fastq