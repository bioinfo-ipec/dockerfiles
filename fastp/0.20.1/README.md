# fastp

This image facilitates the usage of [fastp](https://github.com/OpenGene/fastp), a tool designed to provide fast all-in-one preprocessing for FastQ files. This tool is developed in C++ with multithreading supported to afford high performance.

## Using the fastp image
You should adapt and run the following command: `docker run --rm -v /your/data/dir:/data bioinfoipec/fastp fastp <arguments>`

To see the `fastp` help, just run `docker run --rm bioinfoipec/fastp fastp --help`.

## Test data
To test the previous command, you can access the [following link](https://github.com/OpenGene/fastp).