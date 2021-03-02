# Kraken

This image facilitates the usage of [Kraken](https://ccb.jhu.edu/software/kraken/), a program that is a taxonomic sequence classifier that assigns taxonomic labels to short DNA reads. It does this by examining the k-mers within a read and querying a database with those k-mers.

## Using Kraken image

- Available Kallisto applications names:
  - `kraken`: main scripts.
  - `kraken-build`: Create the standard Kraken database.
  - `kraken-translate`: Produces two different output formats for classified sequences.
  - `kraken-report`: Creates an report for results.
  - `kraken-filter`: Adjusts the confidence score

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/kraken <kraken-application-name> <commands>`

See the [`MANUAL`](https://ccb.jhu.edu/software/kraken/MANUAL.html), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/kraken <kraken-application-name> -h` (e.g. `docker run --rm bioinfoipec/kraken kraken -h`).

## Test data
To test the previous command, you can access the [following link](https://ccb.jhu.edu/software/kraken/MANUAL.html).