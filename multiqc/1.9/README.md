# MultiQC

This image facilitates the usage of [MultiQC](https://multiqc.info), a program that aggregates results from bioinformatics analyses across many samples into a single report.

## Using MultiQC image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/multiqc multiqc <options>`

See the [`MANUAL`](https://multiqc.info/docs/), for more details.

To obtain help you just need to run: `docker run --rm bioinfoipec/multiqc multiqc -h`.

## Test data
To test the previous command, you can access the [following link](https://multiqc.info/docs/#running-multiqc).


