# Bowtie

This image facilitates the usage of [Bowtie](https://bowtie-bio.sourceforge.net/), a program that is an ultrafast, memory-efficient short read aligner geared toward quickly aligning large sets of short DNA sequences (reads) to large genomes. It aligns 35-base-pair reads to the human genome at a rate of 25 million reads per hour on a typical workstation. Bowtie indexes the genome with a Burrows-Wheeler index to keep its memory footprint small: for the human genome, the index is typically about 2.2 GB (for unpaired alignment) or 2.9 GB (for paired-end alignment). Bowtie can also output alignments in the standard SAM format, allowing Bowtie to interoperate with other tools supporting SAM, including the SAMtools consensus, SNP, and indel callers.

## Using Bowtie image

- Available bowtie application names:
  - `bowtie`
  - `bowtie-build`
  - `bowtie-inspect`
  
In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/bowtie <bowtie-application-name> <commands>`

See the [`MANUAL`](http://bowtie-bio.sourceforge.net/manual.shtml), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/bowtie <bowtie-application-name> -h` (e.g. `docker run --rm bioinfoipec/bowtie bowtie -h`).

## Test data
To test the previous command, you can access the [following link](http://bowtie-bio.sourceforge.net/tutorial.shtml).