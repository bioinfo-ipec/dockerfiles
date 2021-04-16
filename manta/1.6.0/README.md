# Manta

This image facilitates the usage of [Manta](https://github.com/Illumina/manta), that is a structural variant and indel caller for mapped sequencing data.

## Using Manta image
In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/manta configManta.py <options>`

See the [`MANUAL`](https://github.com/Illumina/manta/blob/master/docs/userGuide/README.md#extended-use-cases), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/manta configManta.py -h`.

## Test data
To test the previous command, you can access the [following link](https://github.com/Illumina/manta/blob/master/docs/userGuide/installation.md#demo).