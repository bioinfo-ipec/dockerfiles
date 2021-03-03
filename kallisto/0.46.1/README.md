# Kallisto

This image facilitates the usage of [Kallisto](https://pachterlab.github.io/kallisto/), a program for quantifying abundances of transcripts from bulk and single-cell RNA-Seq data, or more generally of target sequences using high-throughput sequencing reads. It is based on the novel idea of pseudoalignment for rapidly determining the compatibility of reads with targets, without the need for alignment. 

## Using Kallisto image

- Available Kallisto modules names:
  - `index`: Builds a kallisto index
  - `quant`: Runs the quantification algorithm
  - `bus`: Generate BUS files for single-cell data
  - `pseudo`: Runs the pseudoalignment step
  - `merge`: Merges several batch runs
  - `h5dump`: Converts HDF5-formatted results to plaintext
  - `inspect`: Inspects and gives information about an index

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/kallisto kallisto <kallisto-module-name> <commands>`

See the [`MANUAL`](https://pachterlab.github.io/kallisto/manual), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/kallisto kallisto <kallisto-module-name> -h` (e.g. `docker run --rm bioinfoipec/kallisto kallisto index -h`).

## Test data
To test the previous command, you can access the [following link](https://pachterlab.github.io/kallisto/starting).


