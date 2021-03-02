# AfterQC
This image facilitates the usage of [AfterQC](https://github.com/OpenGene/AfterQC), a program for automatic filtering, trimming, error removing and quality control of FASTQ files.

## Using the AfterQC image
You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/afterqc afterqc.py -1 /data/input_R1.fq -2 /data/input_R2.fq -g /data/output -b /data/output -r /data/output`

This command will save the output files in `output` directory. With the good reads, bad reads and the report containing the report of quality control.

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the FASTQ file you want to analyze.
- `input.fq` to the actual name of your input file.

To see the `AfterQC` help, just run `docker run --rm bioinfoipec/afterqc afterqc.py --help`.

Note that the fastq file does not need to be descompressed as `AfterQC` can deal with both compressed and uncompressed FASTQ files.

## Test data
To test the previous command, you can use the files in `testdata` directory and type as following:

```bash
docker run --rm -v /dockerfiles/testdata/:/data bioinfoipec/afterqc afterqc.py -1 /data/R1.fq -1 /data/R2.fq -g /data/output -b /data/output -r /data/output
```
