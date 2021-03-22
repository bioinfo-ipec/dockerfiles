# HTSeq

This image facilitates the usage of [HTSeq](https://github.com/htseq/htseq), that is a Python library to facilitate processing and analysis of data from high-throughput sequencing (HTS) experiments.

## Using HTSeq image

In order to use this image you need to run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/htseq htseq-count <arguments>`

See the [`MANUAL`](https://htseq.readthedocs.io/en/master/), for more details.

To obtain help of an tool usage, you just need to run: `docker run --rm bioinfoipec/htseq htseq-count -h`.

## Test data
To test the previous command, you can access the [following link](https://htseq.readthedocs.io/en/master/).