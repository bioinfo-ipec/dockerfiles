# Ensembl VEP

This image facilitates the usage of [VEP](http://www.ensembl.org/info/docs/tools/vep/index.html), a tool that determines the effect of your variants (SNPs, insertions, deletions, CNVs or structural variants) on genes, transcripts, and protein sequence, as well as regulatory regions.

## Using the Ensembl VEP image
You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/ensembl_vep <arguments>`

To see the `ensembl_vep` help, just run `docker run --rm bioinfoipec/ensembl_vep <argument> --help`.

## Test data
To test the previous command, you can access the [following link](http://www.ensembl.org/info/docs/tools/vep/script/index.html).