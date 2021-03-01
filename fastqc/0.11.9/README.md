# FastQC

This image facilitates the usage of [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/), a quality control tool for high throughput sequence data.

## Using the FastQC image
You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/fastqc fastqc /data/input.fq`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the FASTQ file you want to analyze.
- `input.fq` to the actual name of your input file.

To see the `FastQC` help, just run `docker run --rm bioinfoipec/fastqc fastqc --help`.

## Test data
To test the previous command, you can download [this FASTQ compressed file](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?cmd=dload&run_list=SRR1654650&format=fastq) (1.1GB). Note that it does not need to be decompressed as `FastQC` can deal with both compressed and uncompressed FASTQ files. 

In the previous command you just need to replace `/data/input.fq` with `/data/sra_data.fastq.gz`. You can also speed up the execution by adding `-t 4` to tell `FastQC` to use 4 cores (it uses 1 core by default). This command will produce two files containing the `FastQC` reports in the `/data` directory: `sra_data_fastqc.html` and `sra_data_fastqc.zip`.