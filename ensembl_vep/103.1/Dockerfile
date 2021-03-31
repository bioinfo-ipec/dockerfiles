################## BASE IMAGE ######################
FROM continuumio/miniconda:4.7.12

################## METADATA ######################
LABEL base_image="continuumio/miniconda"
LABEL version="latest"
LABEL software="VEP"
LABEL software.version="103.1"
LABEL about.summary="VEP determines the effect of your variants (SNPs, insertions, deletions, CNVs or structural variants) on genes, transcripts, and protein sequence, as well as regulatory regions"
LABEL about.home="http://www.ensembl.org/info/docs/tools/vep/index.html"
LABEL about.documentation="http://www.ensembl.org/info/docs/tools/vep/index.html"
LABEL about.license_file="http://www.ensembl.org/info/docs/tools/vep/index.html"

################## MAINTAINER ######################
MAINTAINER Carlos Biagi Jr <cbiagijr@gmail.com>

################## INSTALLATION ######################
RUN conda install -y -c bioconda ensembl-vep=103.1