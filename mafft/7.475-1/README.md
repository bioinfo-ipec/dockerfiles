# MAFFT

This image facilitates the usage of [MAFFT](https://mafft.cbrc.jp/alignment/software/), that is a multiple alignment program for amino acid or nucleotide sequences.

## Using MAFFT image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/mafft <arguments>`

See the [`MANUAL`](https://mafft.cbrc.jp/alignment/software/), for more details.

To obtain help of an tool usage, you just need to run: `docker run --rm bioinfoipec/mafft -h`.

## Test data
To test the previous command, you can access the [following link](https://mafft.cbrc.jp/alignment/software/).