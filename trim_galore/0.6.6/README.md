# TrimGalore

This image facilitates the usage of [TrimGalore](https://github.com/FelixKrueger/TrimGalore), is a wrapper around Cutadapt and FastQC to consistently apply adapter and quality trimming to FastQ files, with extra functionality for RRBS data.

## Using TrimGalore image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/trim_galore trim_galore [options] <filename(s)>`

See the [`MANUAL`](https://github.com/FelixKrueger/TrimGalore/blob/master/Docs/Trim_Galore_User_Guide.md), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/trim_galore trim_galore -h`.

## Test data
To test the previous command, you can access the [following link](https://github.com/FelixKrueger/TrimGalore/blob/master/Docs/Trim_Galore_User_Guide.md).


