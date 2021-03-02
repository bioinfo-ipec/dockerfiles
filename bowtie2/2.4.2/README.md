# Bowtie2

This image facilitates the usage of [Bowtie2](https://bowtie-bio.sourceforge.net/bowtie2/), a program that is an ultrafast and memory-efficient tool for aligning sequencing reads to long reference sequences. It is particularly good at aligning reads of about 50 up to 100s of characters to relatively long (e.g. mammalian) genomes. Bowtie 2 indexes the genome with an FM Index (based on the Burrows-Wheeler Transform or BWT) to keep its memory footprint small: for the human genome, its memory footprint is typically around 3.2 gigabytes of RAM. Bowtie 2 supports gapped, local, and paired-end alignment modes.

## Using Bowtie2 image

- Available bowtie2 application names:
  - `bowtie2`
  - `bowtie2-align-s`
  - `bowtie2-align-l`
  - `bowtie2-build`
  - `bowtie2-build-s`
  - `bowtie2-build-l`
  - `bowtie2-inspect`
  - `bowtie2-inspect-s`
  - `bowtie2-inspect-l`
  
In order to use this image you need to create a custom database from a multi-FASTA file of sequences with this command: `docker run --rm -v /your/data/dir:/data bioinfoipec/bowtie2 <bowtie2-application-name> <commands>`

See the [`MANUAL`](http://bowtie-bio.sourceforge.net/bowtie2/manual.shtml), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/bowtie2 <bowtie2-application-name> -h` (e.g. `docker run --rm bioinfoipec/bowtie2 bowtie2 -h`).

## Test data
To test the previous command, you can access the [following link](http://bowtie-bio.sourceforge.net/bowtie2/manual.shtml#getting-started-with-bowtie-2-lambda-phage-example).


