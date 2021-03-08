# SnpEff

This image facilitates the usage of [SnpEff](https://pcingola.github.io/SnpEff/), that is a variant annotation and effect prediction tool. It annotates and predicts the effects of genetic variants (such as amino acid changes).

## Using SnpEff image

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/snpEff snpEff <arguments>`

See the [`MANUAL`](https://pcingola.github.io/SnpEff/se_introduction/), for more details.

To obtain help of an tool usage, you just need to run: `docker run --rm bioinfoipec/snpEff snpEff -h`.

## Test data
To test the previous command, you can access the [following link](https://pcingola.github.io/SnpEff/).