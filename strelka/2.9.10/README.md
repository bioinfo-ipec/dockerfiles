# strelka

This image facilitates the usage of [strelka](https://github.com/Illumina/strelka), that calls somatic and germline small variants from mapped sequencing reads.

## Using strelka image

In order to use this image you need to run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/strelka <configureStrelkaGermlineWorkflow.py or configureStrelkaSomaticWorkflow.py> [options]*`

See the [`MANUAL`](https://github.com/Illumina/strelka/blob/v2.9.x/docs/userGuide/README.md), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/strelka <configureStrelkaGermlineWorkflow.py or configureStrelkaSomaticWorkflow.py> -h`.

## Test data
To test the previous command, you can access the [following link](https://github.com/Illumina/strelka/blob/v2.9.x/docs/userGuide/quickStart.md).


