# TopHat2

This image facilitates the usage of [TopHat2](https://ccb.jhu.edu/software/tophat/), is a fast splice junction mapper for RNA-Seq reads. It aligns RNA-Seq reads to mammalian-sized genomes using the ultra high-throughput short read aligner Bowtie, and then analyzes the mapping results to identify splice junctions between exons.

## Using TopHat2 image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/tophat2 tophat [options]* <genome_index_base> <reads1_1[,...,readsN_1]> [reads1_2,...readsN_2]`

See the [`MANUAL`](http://ccb.jhu.edu/software/tophat/manual.shtml), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/tophat2 tophat -h`.

## Test data
To test the previous command, you can access the [following link](https://ccb.jhu.edu/software/tophat/tutorial.shtml).


