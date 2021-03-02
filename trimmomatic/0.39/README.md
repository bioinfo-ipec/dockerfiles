# Trimmomatic

This image facilitates the usage of [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic), is a flexible read trimming tool for Illumina NGS data.

## Using Trimmomatic image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/trimmomatic trimmomatic <PE or SE> [options]`

See the [`MANUAL`](http://www.usadellab.org/cms/?page=trimmomatic), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/trimmomatic trimmomatic -h`.

## Test data
To test the previous command, you can access the [following link](http://www.usadellab.org/cms/?page=trimmomatic).


