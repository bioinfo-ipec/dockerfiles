# cutadapt

## Using the Cutadapt image
You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/cutadapt -u 10 /data/input.fq -o /data/output.fq`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the input file you want to process.
- `input.fq` to the actual name of your input file.
- `output.fq` to the actual name of your output file.

A negative value after `-u` would trims reads at the end.

To see the [Cutadapt](http://cutadapt.readthedocs.io/) help, just run `docker run --rm bioinfoipec/cutadapt cutadapt --help`.

## Test data
To test the previous command, you can download [this FASTQ compressed file](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?cmd=dload&run_list=SRR1654650&format=fastq) (1.1GB). Note that it does not need to be decompressed as `Cutadapt` can deal with both compressed and uncompressed fastq files. 

In the previous command you just need to replace `/data/input.fq` with `/data/sra_data.fastq.gz`. You can also speed up the execution by adding `-j 4` to tell `Cutadapt` to use 4 cores (it uses 1 core by default).

*Note*: processing this file ends up with the following error because of an extra line at the end of the FASTQ, but the `output` file contains the correct result.

```
cutadapt.seqio.FormatError: Line 1 in FASTQ file is expected to start with '@', but found '\n'
cutadapt: error: Line 1 in FASTQ file is expected to start with '@', but found '\n'
```