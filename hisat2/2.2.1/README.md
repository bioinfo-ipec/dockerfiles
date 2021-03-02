# HISAT2

This image facilitates the usage of [HISAT2](http://daehwankimlab.github.io/hisat2/), a program that is a fast and sensitive alignment program for mapping next-generation sequencing reads (both DNA and RNA) to a population of human genomes as well as to a single reference genome.

## Using HISAT2 image

- Available HISAT2 application names:
  - `hisat2`
  - `hisat2-align-s`
  - `hisat2-align-l`
  - `hisat2-build`
  - `hisat2-build-s`
  - `hisat2-build-l`
  - `hisat2-inspect`
  - `hisat2-inspect-s`
  - `hisat2-inspect-l`

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/hisat2 <hisat2-application-name> <commands>`

See the [`MANUAL`](http://daehwankimlab.github.io/hisat2/manual/), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/hisat2 <hisat2-application-name> -h` (e.g. `docker run --rm bioinfoipec/hisat2 hisat2 -h`).

## Test data
To test the previous command, you can access the [following link](http://daehwankimlab.github.io/hisat2/howto/).


