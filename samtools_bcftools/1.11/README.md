# SAMtools

This image facilitates the usage of [SAMtools-BCFtools](http://www.htslib.org/), a suite of programs for interacting with high-throughput sequencing data.

To see `SAMtools-BCFtools` options, just run:  `docker run --rm biagii/samtools_bcftools samtools --help` or `docker run --rm biagii/samtools_bcftools bcftools --help`.

## Using the SAMtools-BCFtools image
You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data biagii/samtools_bcftools <samtools_or_bcftools> <options>`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the input files you want to analyze.
- `<samtools_or_bcftools>` to the name of either `SAMtools` or `BCFtools` executable you want to use.
- `<options> ` with the specific options of the `SAMtools` or `BCFtools` application. These options will include the input/output files, which should be referenced under `/data/`.

For instance, if you want to generate a high quality VCF file from an input SAM file, you should run the following three steps: 

- `docker run --rm -v /your/data/dir:/data biagii/samtools_bcftools samtools view -bS /data/aln-pe.sam > aln-pe.bam`

- `docker run --rm -v /your/data/dir:/data biagii/samtools_bcftools bash -c "samtools mpileup -uf /data/chr19_KI270866v1_alt.fasta /data/aln-pe.bam | bcftools call -mv > /data/var.raw.vcf"`

- `docker run --rm -v /your/data/dir:/data biagii/samtools_bcftools bash -c "bcftools filter -s LowQual -e '%QUAL<20 || DP>100' /data/var.raw.vcf  > /data/var.flt.vcf"`

## Test data
To test the previous commands, the input SAM file and the input FASTA file are available in `testdata` directory.