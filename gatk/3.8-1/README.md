# GATK 3

This image facilitates the usage of [GATK 3](https://gatk.broadinstitute.org/hc/en-us), the industry standard for identifying SNPs and indels in germline DNA and RNAseq data. Its scope is now expanding to include somatic short variant calling, and to tackle copy number (CNV) and structural variation (SV). In addition to the variant callers themselves, the GATK also includes many utilities to perform related tasks such as processing and quality control of high-throughput sequencing data, and bundles the popular Picard toolkit.

## Using the GATK 3 image
To see `GATK 3` options and available tools, just run `docker run --rm broadinstitute/gatk3:3.8-1 java -jar /opt/GenomeAnalysisTK.jar -h`.

You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data broadinstitute/gatk3:3.8-1 java -jar /opt/GenomeAnalysisTK.jar <tools> <options>`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the input files you want to analyze.
- `<tools>` to the name of the `GATK 3` tool you want to use.
- `<options> ` with the specific options of the `GATK 3` tool. These options will include the input/output files, which should be referenced under `/data/`.

For instance, to generate a target list of InDel positions using `GATK 3`, you should run: `docker run --rm -v /your/data/dir:/data broadinstitute/gatk3:3.8-1 java -jar /opt/GenomeAnalysisTK.jar -T RealignerTargetCreator -R /data/chr19_KI270866v1_alt.fasta -I /data/aln-pe_out_sorted.bam -o /data/aln-pe_out_sorted.list`

## Test data
To test the previous command, all the required files in `testdata` directory.