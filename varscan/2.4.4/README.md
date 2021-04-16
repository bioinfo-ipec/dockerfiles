# VarScan

This image facilitates the usage of [VarScan](http://varscan.sourceforge.net), that is a variant calling and somatic mutation/CNV detection for next-generation sequencing data.

## Using VarScan image

In order to use this image you need to run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/varscan <COMMAND> [options]*`

See the [`MANUAL`](http://varscan.sourceforge.net/using-varscan.html), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/varscan <COMMAND> -h`.

## Test data
To test the previous command, you can access the [following link](http://varscan.sourceforge.net/using-varscan.html).


