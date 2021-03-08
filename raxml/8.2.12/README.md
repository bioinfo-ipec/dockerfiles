# RAxML

This image facilitates the usage of [RAxML](https://cme.h-its.org/exelixis/web/software/raxml/), that is a program for sequential and parallel Maximum Likelihood based inference of large phylogenetic trees. It can also be used for post- analyses of sets of phylogenetic trees, analyses of alignments and, evolutionary placement of short reads.

## Using RAxML image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/raxml RAxML <arguments>`

See the [`MANUAL`](https://cme.h-its.org/exelixis/resource/download/NewManual.pdf), for more details.

To obtain help of an tool usage, you just need to run: `docker run --rm bioinfoipec/raxml RAxML -h`.

## Test data
To test the previous command, you can access the [following link](https://cme.h-its.org/exelixis/web/software/raxml/).