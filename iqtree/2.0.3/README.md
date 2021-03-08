# IQ-TREE

This image facilitates the usage of [IQ-TREE](http://www.iqtree.org), that is a efficient phylogenomic software by maximum likelihood.

## Using IQ-TREE image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/iqtree iqtree <arguments>`

See the [`MANUAL`](http://www.iqtree.org/doc/iqtree-doc.pdf), for more details.

To obtain help of an tool usage, you just need to run: `docker run --rm bioinfoipec/iqtree iqtree -h`.

## Test data
To test the previous command, you can access the [following link](http://www.iqtree.org).