# GCTA

This image facilitates the usage of [GCTA](https://cnsgenomics.com/software/gcta/), that is a a tool for Genome-wide Complex Trait Analysis.

## Using GCTA image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/gcta gcta <arguments>`

See the [`MANUAL`](https://cnsgenomics.com/software/gcta/), for more details.

To obtain help of an tool usage, you just need to run: `docker run --rm bioinfoipec/gcta gcta -h`.

## Test data
To test the previous command, you can access the [following link](https://cnsgenomics.com/software/gcta/).