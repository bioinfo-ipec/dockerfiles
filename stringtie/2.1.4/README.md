# StringTie

This image facilitates the usage of [StringTie](https://ccb.jhu.edu/software/stringtie/), is a fast and highly efficient assembler program of RNA-Seq alignments into potential transcripts. It uses a novel network flow algorithm as well as an optional de novo assembly step to assemble and quantitate full-length transcripts representing multiple splice variants for each gene locus.

## Using StringTie image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/stringtie <aligned_reads.bam> [options]*`

See the [`MANUAL`](https://ccb.jhu.edu/software/stringtie/index.shtml?t=manual), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/stringtie -h`.

## Test data
To test the previous command, you can access the [following link](https://ccb.jhu.edu/software/stringtie/index.shtml?t=manual).


