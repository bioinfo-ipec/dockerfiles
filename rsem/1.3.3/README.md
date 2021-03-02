# RSEM

This image facilitates the usage of [RSEM](https://github.com/deweylab/RSEM), a program for accurate quantification of gene and isoform expression from RNA-Seq data.

## Using RSEM image

- Available RSEM applications names:
  - `rsem-prepare-reference`: Prepares the reference sequences
  - `rsem-calculate-expression`: Calculate expression values
  - `rsem-tbam2gbam`: Converts transcript BAM file into genome BAM file
  - `rsem-bam2wig`: Generates a Wiggle file
  - `rsem-plot-transcript-wiggles`: Generates Transcript Wiggle Plots
  - `rsem-plot-model`: Visualizes the model learned by RSEM

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/rsem <rsem-application-name> <commands>`

See the [`MANUAL`](https://github.com/deweylab/RSEM), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/rsem <rsem-application-name> -h` (e.g. `docker run --rm bioinfoipec/rsem rsem-prepare-reference -h`).

## Test data
To test the previous command, you can access the [following link](https://github.com/deweylab/RSEM#example-main).


