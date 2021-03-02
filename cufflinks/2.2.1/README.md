# Cufflinks

This image facilitates the usage of [Cufflinks](http://cole-trapnell-lab.github.io/cufflinks/), a program that assembles transcripts, estimates their abundances, and tests for differential expression and regulation in RNA-Seq samples. It accepts aligned RNA-Seq reads and assembles the alignments into a parsimonious set of transcripts. Cufflinks then estimates the relative abundances of these transcripts based on how many reads support each one, taking into account biases in library preparation protocols.

## Using Cufflinks image

- Available modules in Cufflinks bowtie2 application names:
  - `Cuffcompare`: After assembling a transcriptome from one or more samples, you’ll probably want to compare your assembly to known transcripts. Even if there is no “reference” transcriptome for the organism you’re studying, you may want to compare the transcriptomes assembled from different RNA-Seq libraries. Cuffcompare helps you perform these comparisons and assess the quality of your assembly.
  - `Cuffmerge`: When you have multiple RNA-Seq libraries and you’ve assembled transcriptomes from each of them, we recommend that you merge these assemblies into a master transcriptome. This step is required for a differential expression analysis of the new transcripts you’ve assembled. Cuffmerge performs this merge step.
  - `Cuffquant`: Quantifying gene and transcript expression in RNA-Seq samples can be computationally expensive. Cuffquant allows you to compute the gene and transcript expression profiles and save these profiles to files that you can analyze later with Cuffdiff or Cuffnorm. This can help you distribute your computational load over a cluster and is recommended for analyses involving more than a handful of libraries.
  - `Cuffdiff`: Comparing expression levels of genes and transcripts in RNA-Seq experiments is a hard problem. Cuffdiff is a highly accurate tool for performing these comparisons, and can tell you not only which genes are up- or down-regulated between two or more conditions, but also which genes are differentially spliced or are undergoing other types of isoform-level regulation.
  - `Cuffnorm`: Sometimes, all you want to do is normalize the expression levels from a set of RNA-Seq libraries so that they’re all on the same scale, facilitating downstream analyses such as clustering. Expression levels reported by Cufflinks in FPKM units are usually comparable between samples, but in certain situations, applying an extra level of normalization can remove sources of bias in the data. Cuffnorm normalizes a set of samples to be on as similar scales as possible, which can improve the results you obtain with other downstream tools.

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/cufflinks <cufflinks-module-name> <commands>`

See the [`MANUAL`](http://cole-trapnell-lab.github.io/cufflinks/manual/), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/cufflinks <cufflinks-module-name> -h` (e.g. `docker run --rm bioinfoipec/cufflinks cufflinks -h`).

## Test data
To test the previous command, you can access the [following link](http://cole-trapnell-lab.github.io/cufflinks/getting_started/).


