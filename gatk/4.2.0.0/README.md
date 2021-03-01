# GATK 4

This image facilitates the usage of [GATK 4](https://gatk.broadinstitute.org/hc/en-us), the industry standard for identifying SNPs and indels in germline DNA and RNAseq data. Its scope is now expanding to include somatic short variant calling, and to tackle copy number (CNV) and structural variation (SV). In addition to the variant callers themselves, the GATK also includes many utilities to perform related tasks such as processing and quality control of high-throughput sequencing data, and bundles the popular Picard toolkit.

## Using the GATK 4 image

To see `GATK 4` available tools, just run `docker run --rm broadinstitute/gatk:4.2.0.0 gatk --list`. Please note that `GATK 4` does not include some tools that are included in [GATK 3](https://hub.docker.com/r/pegi3s/gatk-3).

To obtain the help of a particular tool, you just need to run: `docker run --rm broadinstitute/gatk:4.2.0.0 gatk <tools> --help` (e.g. `docker run --rm broadinstitute/gatk:4.2.0.0 gatk SortVcf --help`)

You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data broadinstitute/gatk:4.2.0.0 gatk <tools> <options>`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the input files you want to analyze.
- `<tools>` to the name of the `GATK 4` tool you want to use.
- `<options> ` with the specific options of the `GATK 4` tool. These options will include the input/output files, which should be referenced under `/data/`.

For instance, to sort a VCF file using `GATK 4`, you should run: `docker run --rm -v /your/data/dir:/data broadinstitute/gatk:4.2.0.0 gatk SortVcf -I /data/test.recode.vcf -O /data/test_sorted.recode.vcf`

## Test data
To test the previous command, the VCF file used is available in `testdata` directory.


