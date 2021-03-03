################## BASE IMAGE ######################
FROM czentye/matplotlib-minimal:3.1.2

################## METADATA ######################
LABEL base_image="czentye/matplotlib-minimal:3.1.2"
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
WORKDIR /tmp
RUN wget https://github.com/ewels/MultiQC/archive/v1.9.zip && \
    unzip v1.9.zip && \
    rm -rf v1.9.zip

WORKDIR /tmp/MultiQC-1.9
RUN python -m pip install .

WORKDIR /