# SUBREAD

This image facilitates the usage of [SUBREAD](http://subread.sourceforge.net), that is a high-performance read alignment, quantification and mutation discovery.

## Using SUBREAD image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/subread <module> [options]*`

See the [`MANUAL`](http://bioinf.wehi.edu.au/subread-package/SubreadUsersGuide.pdf), for more details.

To obtain abbreviated help of an application, you just need to run: `docker run --rm bioinfoipec/subread -h`.

## Test data
To test the previous command, you can access the [following link](http://bioinf.wehi.edu.au/subread-package/SubreadUsersGuide.pdf).