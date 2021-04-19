# Short Alignment Marking

This image facilitates the usage of [Short Alignment Marking](https://github.com/nygenome/nygc-short-alignment-marking), that is a tool that parses the bam file and marks as unmapped a read with alignment length below a user-defined threshold. Reads are not filtered from the bam file but kept as unmapped.

## Using Short Alignment Marking image
In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/short-alignment-marking filter_bam <options>`

See the [`MANUAL`](https://github.com/nygenome/nygc-short-alignment-marking), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/short-alignment-marking filter_bam --help`.

## Test data
To test the previous command, you can access the [following link](https://github.com/nygenome/nygc-short-alignment-marking).