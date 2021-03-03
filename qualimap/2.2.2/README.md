# Qualimap

This image facilitates the usage of [QualiMap](http://qualimap.bioinfo.cipf.es/), a platform-independent application to facilitate the quality control of alignment sequencing data.

## Using the QualiMap image

Supported types of experiments include:

- Whole-genome sequencing.
- Whole-exome sequencing.
- RNA-seq.
- ChIP-seq.

By running the command `docker run --rm -v /your/data/dir:/data bioinfoipec/qualimap qualimap -h` you can list the tools included in this suite, namely:

- `bamqc`: evaluate NGS mapping to a reference genome.
- `rnaseq`: evaluate RNA-seq alignment data.
- `counts`: counts data analysis (further RNA-seq data evaluation).
- `multi-bamqc`: compare QC reports from multiple NGS mappings.
- `clustering`: cluster epigenomic signals.
- `comp-counts`: compute feature counts.

To obtain the help of a particular tool, you just need to run: `docker run --rm -v /your/data/dir:/data bioinfoipec/qualimap qualimap <tools>` (e.g. `docker run --rm -v /your/data/dir:/data bioinfoipec/qualimap qualimap bamqc`)

You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/qualimap qualimap <tools> <options>`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the input file you want to analyze.
- `<tools>` to the name of the `QualiMap` tool you want to use.
- `<options>` with the specific options of the `QualiMap` tool. These options will include the input/output files, which should be referenced under `/data/`.

For instance, to use the `bamqc` tool with `HG00096.chrom20.bam` alignment with 400 windows and size of a homopolymer = 3, you should run: `docker run --rm -v /your/data/dir:/data bioinfoipec/qualimap qualimap bamqc -bam /data/HG00096.chrom20.bam -c -nw 400 -hm 3`

## Test data
To test the previous command, the sequence alignment file used is available [here](http://qualimap.bioinfo.cipf.es/samples/alignments/HG00096.chrom20.bam).