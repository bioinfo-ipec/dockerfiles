# SRA Toolkit

This image allows the usage of the [SRA Toolkit](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=toolkit_doc) suite. Frequently used tools in this suite are:

## Using the SRA Toolkit image

- `fastq-dump`: convert SRA data into fastq format.
- `fasterq-dump`: convert SRA data into fastq format (faster than `fastq-dump`).
- `prefetch`: allows command-line downloading of SRA, dbGaP, and ADSP data.
- `sam-dump`: convert SRA data to sam format.
- `sra-pileup`: generate pileup statistics on aligned SRA data.
- `vdb-config`: display and modify VDB configuration information.
- `vdb-decrypt`: decrypt non-SRA dbGaP data ("phenotype data").

Additional tools included in this suite are:

- `abi-dump`: convert SRA data into ABI format (csfasta / qual).
- `illumina-dump`: convert SRA data into Illumina native formats (qseq, etc.).
- `sff-dump`: convert SRA data to sff format.
- `sra-stat`: generate statistics about SRA data (quality distribution, etc.).
- `vdb-dump`: output the native VDB format of SRA data.
- `vdb-encrypt`: encrypt non-SRA dbGaP data ("phenotype data").
- `vdb-validate`: validate the integrity of downloaded SRA data.

To obtain the help of an application, you just need to run: `docker run --rm ncbi/sra-tools:2.10.8 <sratoolkit-application-name> --help` (e.g. `docker run --rm ncbi/sra-tools:2.10.8 fastq-dump --help`)

To run an application, you should adapt and run the following command: `docker run --rm -v /your/data/dir:/data ncbi/sra-tools:2.10.8 <sratoolkit-application-name> /data/mydata.sra --outdir /data/outdir`

In this command, you should replace:
- `/your/data/dir` to point to the directory that contains the SRA file you want to convert into a FASTQ file.
- `<sratoolkit-application-name>` to the name of the `SRA Toolkit` application you want to use.
- `mydata.sra` to the actual name of your input file.
- `outdir` to the actual name of your output directory.

For instance, to download data SRR6175516 using the `fastq-dump` application, you should run: `docker run --rm -v /your/data/dir:/data ncbi/sra-tools:2.10.8 fastq-dump SRR6175516 --outdir /data`

*Note*: Depending on DNS restrictions from your firewall institution, you may obtain an error message:

```
fastq-dump.2.10.0 sys: connection busy while validating within network system module - Failed to Make Connection in KClientHttpOpen to 'www.ncbi.nlm.nih.gov:443
```

In order to solve it, you need to change your DNS Address. Please follow the steps provided [here](https://github.com/hlfernandez/til/blob/master/docker/fix-dns-problems.md).