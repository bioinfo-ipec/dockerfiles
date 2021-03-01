# bwa

This image facilitates the usage of [BWA](http://bio-bwa.sourceforge.net/), a software package for mapping low-divergent sequences against a large reference genome, such as the human genome. It consists of three algorithms: `BWA-backtrack`, `BWA-SW` and `BWA-MEM`. The first algorithm is designed for Illumina sequence reads up to `100bp`, while the remaining two for `70bp` to `1Mbp` sequences. `BWA-MEM` and `BWA-SW` share similar features such as long-read support and split alignment, but `BWA-MEM`, which is the latest, is generally recommended for high-quality queries as it is faster and more accurate. `BWA-MEM` also has better performance than `BWA-backtrack` for `70-100bp` Illumina reads.

To see `BWA` options, just run `docker run --rm bioinfoipec/bwa bwa`.

## Using the BWA image

You should adapt and run the following command: `docker run --rm -v "/your/data/dir:/data" bioinfoipec/bwa bwa <command> <options>`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the FASTA file you want to analyze.
- `<command>` with the specific command of the `BWA` tool. 
- `<options>` with the specific options of the `BWA` tool. These options will include the input/output files, which should be referenced under `/data/`.

For instance, if you want to align with the `BWA-MEM` algorithm the reads `7859_GPI.read1.fq` and `7859_GPI.read2.fq` with the chromosome `chr19_KI270866v1_alt.fasta`, you should run: `docker run --rm -v "/your/data/dir:/data" bioinfoipec/bwa bwa mem /data/chr19_KI270866v1_alt.fasta /data/7859_GPI.read1.fq /data/7859_GPI.read2.fq > aln-pe.sam`

### *Note*
Before executing the previous command, it is necessary to generate the index files of the sequence `chr19_KI270866v1_alt.fasta`. To do so, you should run: `docker run --rm -v "/your/data/dir:/data" bioinfoipec/bwa bwa index /data/chr19_KI270866v1_alt.fasta`

## Test data
To test the previous commands, the input FASTA file used is available [here](https://raw.githubusercontent.com/cbioinfoipec/dockerfiles/master/bwa/0.7.17/testdata/chr19_KI270866v1_alt.fasta).
The two FASTQ files used, one for each mate of the paired reads, are available [here](https://raw.githubusercontent.com/cbioinfoipec/dockerfiles/master/bwa/0.7.17/testdata/7859_GPI.read1.fq) and [here](https://raw.githubusercontent.com/cbioinfoipec/dockerfiles/master/bwa/0.7.17/testdata/7859_GPI.read2.fq).