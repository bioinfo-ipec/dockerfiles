# bcl2fastq

This image facilitates the usage of [bcl2fastq](https://support.illumina.com/sequencing/sequencing_software/bcl2fastq-conversion-software.html), is a tool that converts both demultiplexes data and converts BCL files generated by Illumina sequencing systems to standard FASTQ file formats for downstream analysis.

## Using bcl2fastq image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/bcl2fastq bcl2fastq [options]`

See the [`MANUAL`](https://support.illumina.com/content/dam/illumina-support/documents/documentation/software_documentation/bcl2fastq/bcl2fastq2-v2-20-software-guide-15051736-03.pdf), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/bcl2fastq bcl2fastq -h`.

## Test data
To test the previous command, you can access the [following link](https://support.illumina.com/content/dam/illumina-support/documents/documentation/software_documentation/bcl2fastq/bcl2fastq2-v2-20-software-guide-15051736-03.pdf).

