# vcflib

This image facilitates the usage of [vcflib](https://github.com/vcflib/vcflib), that is a C++ library and cmdline tools for parsing and manipulating VCF files.

## Using vcflib image

### Tools
#### filter

| filter command | description |
| :-------------- | :---------- |
 | [vcfuniq](https://github.com/vcflib/vcflib/blob/master/doc/vcfuniq.md) | List unique genotypes. Like GNU uniq, but for VCF records. Remove records which have the same position, ref, and alt as the previous record. |
 | [vcfuniqalleles](https://github.com/vcflib/vcflib/blob/master/doc/vcfuniqalleles.md) | List unique alleles For each record, remove any duplicate alternate alleles that may have resulted from merging separate VCF files. |
 | [vcffilter](https://github.com/vcflib/vcflib/blob/master/doc/vcffilter.md) | VCF filter the specified vcf file using the set of filters |

#### metrics

| metrics command | description |
| :-------------- | :---------- |
 | [vcfcheck](https://github.com/vcflib/vcflib/blob/master/doc/vcfcheck.md) | Validate integrity and identity of the VCF by verifying that the VCF record's REF matches a given reference file. |
 | [vcfhethomratio](https://github.com/vcflib/vcflib/blob/master/doc/vcfhethomratio.md) | Generates the het/hom ratio for each individual in the file |
 | [vcfhetcount](https://github.com/vcflib/vcflib/blob/master/doc/vcfhetcount.md) | Calculate the heterozygosity rate: count the number of alternate alleles in heterozygous genotypes in all records in the vcf file |
 | [vcfdistance](https://github.com/vcflib/vcflib/blob/master/doc/vcfdistance.md) | Adds a tag to each variant record which indicates the distance to the nearest variant. (defaults to BasesToClosestVariant if no custom tag name is given. |
 | [vcfentropy](https://github.com/vcflib/vcflib/blob/master/doc/vcfentropy.md) | Annotate VCF records with the Shannon entropy of flanking sequence. Anotates the output VCF file with, for each record, EntropyLeft, EntropyRight, EntropyCenter, which are the entropies of the sequence of the given window size to the left, right, and center of the record. Also adds EntropyRef and EntropyAlt for each alt. |

#### phenotype

| phenotype command | description |
| :-------------- | :---------- |
 | [permuteGPAT++](https://github.com/vcflib/vcflib/blob/master/doc/permuteGPAT++.md) | **permuteGPAT++** is a method for adding empirical p-values to a GPAT++ score. |

#### genotype

| genotype command | description |
| :-------------- | :---------- |
 | [normalize-iHS](https://github.com/vcflib/vcflib/blob/master/doc/normalize-iHS.md) | normalizes iHS or XP-EHH scores. |
 | [hapLrt](https://github.com/vcflib/vcflib/blob/master/doc/hapLrt.md) | HapLRT is a likelihood ratio test for haplotype lengths. The lengths are modeled with an exponential distribution. The sign denotes if the target has longer haplotypes (1) or the background (-1). |
 | [abba-baba](https://github.com/vcflib/vcflib/blob/master/doc/abba-baba.md) | **abba-baba** calculates the tree pattern for four indviduals. This tool assumes reference is ancestral and ignores non **abba-baba** sites. The output is a boolian value: 1 = true , 0 = false for abba and baba. the tree argument should be specified from the most basal taxa to the most derived. |

#### transformation

| transformation command | description |
| :-------------- | :---------- |
 | [vcfinfo2qual](https://github.com/vcflib/vcflib/blob/master/doc/vcfinfo2qual.md) | Sets QUAL from info field tag keyed by [key]. The VCF file may be omitted and read from stdin. The average of the field is used if it contains multiple values. |
 | [vcfsamplediff](https://github.com/vcflib/vcflib/blob/master/doc/vcfsamplediff.md) | Establish putative somatic variants using reported differences between germline and somatic samples. Tags each record where the listed sample genotypes differ with <tag>. The first sample is assumed to be germline, the second somatic. Each record is tagged with <tag>={germline,somatic,loh} to specify the type of variant given the genotype difference between the two samples. |
 | [vcfaddinfo](https://github.com/vcflib/vcflib/blob/master/doc/vcfaddinfo.md) | Adds info fields from the second file which are not present in the first vcf file. |
 | [vcfremoveaberrantgenotypes](https://github.com/vcflib/vcflib/blob/master/doc/vcfremoveaberrantgenotypes.md) | strips samples which are homozygous but have observations implying heterozygosity. Remove samples for which the reported genotype (GT) and observation counts disagree (AO, RO). |
 | [vcfglxgt](https://github.com/vcflib/vcflib/blob/master/doc/vcfglxgt.md) | Set genotypes using the maximum genotype likelihood for each sample. |
 | [dumpContigsFromHeader](https://github.com/vcflib/vcflib/blob/master/doc/dumpContigsFromHeader.md) | Dump contigs from header |
 | [vcfevenregions](https://github.com/vcflib/vcflib/blob/master/doc/vcfevenregions.md) | Generates a list of regions, e.g. chr20:10..30 using the variant density information provided in the VCF file to ensure that the regions have even numbers of variants. This can be use to reduce the variance in runtime when dividing variant detection or genotyping by genomic coordinates. |
 | [vcfcat](https://github.com/vcflib/vcflib/blob/master/doc/vcfcat.md) | Concatenates VCF files |
 | [vcfannotategenotypes](https://github.com/vcflib/vcflib/blob/master/doc/vcfannotategenotypes.md) | Examine genotype correspondence. Annotate genotypes in the first file with genotypes in the second adding the genotype as another flag to each sample filed in the first file. annotation-tag is the name of the sample flag which is added to store the annotation. also adds a 'has_variant' flag for sites where the second file has a variant. |
 | [vcfafpath](https://github.com/vcflib/vcflib/blob/master/doc/vcfafpath.md) | Display genotype paths |
 | [vcfclassify](https://github.com/vcflib/vcflib/blob/master/doc/vcfclassify.md) | Creates a new VCF where each variant is tagged by allele class: snp, ts/tv, indel, mnp |
 | [vcfallelicprimitives](https://github.com/vcflib/vcflib/blob/master/doc/vcfallelicprimitives.md) | If multiple allelic primitives (gaps or mismatches) are specified in a single VCF record, split the record into multiple lines, but drop all INFO fields. Does not handle genotypes (yet). MNPs are split into multiple SNPs unless the -m flag is provided. Records generated by splits have th |
 | [vcfqual2info](https://github.com/vcflib/vcflib/blob/master/doc/vcfqual2info.md) | Puts QUAL into an info field tag keyed by [key]. |
 | [vcfcreatemulti](https://github.com/vcflib/vcflib/blob/master/doc/vcfcreatemulti.md) | If overlapping alleles are represented across multiple records, merge them into a single record. Currently only for indels. |
 | [vcfgeno2alleles](https://github.com/vcflib/vcflib/blob/master/doc/vcfgeno2alleles.md) | modifies the genotypes field to provide the literal alleles rather than indexes |
 | [vcfsample2info](https://github.com/vcflib/vcflib/blob/master/doc/vcfsample2info.md) | Take annotations given in the per-sample fields and add the mean, median, min, or max to the site-level INFO. |
 | [vcfld](https://github.com/vcflib/vcflib/blob/master/doc/vcfld.md) | Compute LD |
 | [vcfnumalt](https://github.com/vcflib/vcflib/blob/master/doc/vcfnumalt.md) | outputs a VCF stream where NUMALT has been generated for each record using sample genotypes |
 | [vcfstreamsort](https://github.com/vcflib/vcflib/blob/master/doc/vcfstreamsort.md) | Sorts the input (either stdin or file) using a streaming sort algorithm. Guarantees that the positional order is correct provided out-of-order variants are no more than 100 positions in the VCF file apart. |
 | [vcfinfosummarize](https://github.com/vcflib/vcflib/blob/master/doc/vcfinfosummarize.md) | Take annotations given in the per-sample fields and add the mean, median, min, or max to the site-level INFO. |
 | [vcflength](https://github.com/vcflib/vcflib/blob/master/doc/vcflength.md) | Add length info field |
 | [vcfkeepgeno](https://github.com/vcflib/vcflib/blob/master/doc/vcfkeepgeno.md) | Reduce file size by removing FORMAT fields not listed on the command line from sample specifications in the output |
 | [vcfcombine](https://github.com/vcflib/vcflib/blob/master/doc/vcfcombine.md) | Combine VCF files positionally, combining samples when sites and alleles are identical. Any number of VCF files may be combined. The INFO field and other columns are taken from one of the files which are combined when records in multiple files match. Alleles must have identical ordering to be combined into one record. If they do not, multiple records will be emitted. |
 | [vcfprimers](https://github.com/vcflib/vcflib/blob/master/doc/vcfprimers.md) | For each VCF record, extract the flanking sequences, and write them to stdout as FASTA records suitable for alignment. |
 | [vcfflatten](https://github.com/vcflib/vcflib/blob/master/doc/vcfflatten.md) | Removes multi-allelic sites by picking the most common alternate. Requires allele frequency specification 'AF' and use of 'G' and 'A' to specify the fields which vary according to the Allele or Genotype. VCF file may be specified on the command line or piped as stdin. |
 | [vcf2dag](https://github.com/vcflib/vcflib/blob/master/doc/vcf2dag.md) | Modify VCF to be able to build a directed acyclic graph (DAG) |
 | [vcfcleancomplex](https://github.com/vcflib/vcflib/blob/master/doc/vcfcleancomplex.md) | Removes reference-matching sequence from complex alleles and adjusts records to reflect positional change. |
 | [vcfbreakmulti](https://github.com/vcflib/vcflib/blob/master/doc/vcfbreakmulti.md) | If multiple alleles are specified in a single record, break the record into multiple lines, preserving allele-specific INFO fields. |
 | [vcfindex](https://github.com/vcflib/vcflib/blob/master/doc/vcfindex.md) | Adds an index number to the INFO field (id=position) |
 | [vcfkeepinfo](https://github.com/vcflib/vcflib/blob/master/doc/vcfkeepinfo.md) | To decrease file size remove INFO fields not listed on the command line |
 | [vcfgeno2haplo](https://github.com/vcflib/vcflib/blob/master/doc/vcfgeno2haplo.md) | Convert genotype-based phased alleles within --window-size into haplotype alleles. Will break haplotype construction when encountering non-phased genotypes on input. |
 | [vcfintersect](https://github.com/vcflib/vcflib/blob/master/doc/vcfintersect.md) | VCF set analysis |
 | [vcfannotate](https://github.com/vcflib/vcflib/blob/master/doc/vcfannotate.md) | Intersect the records in the VCF file with targets provided in a BED file. Intersections are done on the reference sequences in the VCF file. If no VCF filename is specified on the command line (last argument) the VCF read from stdin. |
 | [smoother](https://github.com/vcflib/vcflib/blob/master/doc/smoother.md) | smoothes is a method for window smoothing many of the GPAT++ formats. |
 | [vcf2fasta](https://github.com/vcflib/vcflib/blob/master/doc/vcf2fasta.md) | Generates sample_seq:N.fa for each sample, reference sequence, and chromosomal copy N in [0,1... ploidy]. Each sequence in the fasta file is named using the same pattern used for the file name, allowing them to be combined. |
 | [vcfsamplenames](https://github.com/vcflib/vcflib/blob/master/doc/vcfsamplenames.md) | List sample names |
 | [vcfleftalign](https://github.com/vcflib/vcflib/blob/master/doc/vcfleftalign.md) | Left-align indels and complex variants in the input using a pairwise ref/alt alignment followed by a heuristic, iterative left realignment process that shifts indel representations to their absolute leftmost (5') extent. |
 | [vcfglbound](https://github.com/vcflib/vcflib/blob/master/doc/vcfglbound.md) | Adjust GLs so that the maximum GL is 0 by dividing all GLs for each sample by the max. |
 | [vcfcommonsamples](https://github.com/vcflib/vcflib/blob/master/doc/vcfcommonsamples.md) | Generates each record in the first file, removing samples not present in the second |
 | [vcfecho](https://github.com/vcflib/vcflib/blob/master/doc/vcfecho.md) | Echo VCF to stdout (simple demo) |
 | [vcfkeepsamples](https://github.com/vcflib/vcflib/blob/master/doc/vcfkeepsamples.md) | outputs each record in the vcf file, removing samples not listed on the command line |
 | [vcf2tsv](https://github.com/vcflib/vcflib/blob/master/doc/vcf2tsv.md) | Converts VCF to per-allelle or per-genotype tab-delimited format, using null string to replace empty values in the table. Specifying -g will output one line per sample with genotype information. When there is more than one alt allele there will be multiple rows, one for each allele and, the info will match the 'A' index |
 | [vcfoverlay](https://github.com/vcflib/vcflib/blob/master/doc/vcfoverlay.md) | Overlay records in the input vcf files with order as precedence. |
 | [vcfgenosamplenames](https://github.com/vcflib/vcflib/blob/master/doc/vcfgenosamplenames.md) | Get samplenames |
 | [vcfremovesamples](https://github.com/vcflib/vcflib/blob/master/doc/vcfremovesamples.md) | outputs each record in the vcf file, removing samples listed on the command line |
 | [vcfremap](https://github.com/vcflib/vcflib/blob/master/doc/vcfremap.md) | For each alternate allele, attempt to realign against the reference with lowered gap open penalty. If realignment is possible, adjust the cigar and reference/alternate alleles. Observe how different alignment parameters, including context and entropy-dependent ones, influence variant classification and interpretation. |
 | [vcffixup](https://github.com/vcflib/vcflib/blob/master/doc/vcffixup.md) | Generates a VCF stream where AC and NS have been generated for each record using sample genotypes |

#### statistics

| statistics command | description |
| :-------------- | :---------- |
 | [vcfgenosummarize](https://github.com/vcflib/vcflib/blob/master/doc/vcfgenosummarize.md) | Adds summary statistics to each record summarizing qualities reported in called genotypes. Uses: RO (reference observation count), QR (quality sum reference observations) AO (alternate observation count), QA (quality sum alternate observations) |
 | [vcfcountalleles](https://github.com/vcflib/vcflib/blob/master/doc/vcfcountalleles.md) | Count alleles |
 | [meltEHH](https://github.com/vcflib/vcflib/blob/master/doc/meltEHH.md) |  |
 | [genotypeSummary](https://github.com/vcflib/vcflib/blob/master/doc/genotypeSummary.md) | Generates a table of genotype counts. Summarizes genotype counts for bi-allelic SNVs and indel |
 | [vcfrandomsample](https://github.com/vcflib/vcflib/blob/master/doc/vcfrandomsample.md) | Randomly sample sites from an input VCF file, which may be provided as stdin. Scale the sampling probability by the field specified in KEY. This may be used to provide uniform sampling across allele frequencies, for instance. |
 | [pVst](https://github.com/vcflib/vcflib/blob/master/doc/pVst.md) | **pVst** calculates vst, a measure of CNV stratification. |
 | [vcfrandom](https://github.com/vcflib/vcflib/blob/master/doc/vcfrandom.md) | Generate a random VCF file |
 | [segmentFst](https://github.com/vcflib/vcflib/blob/master/doc/segmentFst.md) | **segmentFst** creates genomic segments (bed file) for regions with high wcFst |
 | [sequenceDiversity](https://github.com/vcflib/vcflib/blob/master/doc/sequenceDiversity.md) | The **sequenceDiversity** program calculates two popular metrics of haplotype diversity: pi and extended haplotype homozygoisty (eHH). Pi is calculated using the Nei and Li 1979 formulation. eHH a convenient way to think about haplotype diversity. When eHH = 0 all haplotypes in the window are unique and when eHH = 1 all haplotypes in the window are identical. |
 | [segmentIhs](https://github.com/vcflib/vcflib/blob/master/doc/segmentIhs.md) | Creates genomic segments (bed file) for regions with high wcFst |
 | [vcfgenotypes](https://github.com/vcflib/vcflib/blob/master/doc/vcfgenotypes.md) | Report the genotypes for each sample, for each variant in the VCF. Convert the numerical represenation of genotypes provided by the GT field to a human-readable genotype format. |
 | [vcfaltcount](https://github.com/vcflib/vcflib/blob/master/doc/vcfaltcount.md) | count the number of alternate alleles in all records in the vcf file |
 | [plotHaps](https://github.com/vcflib/vcflib/blob/master/doc/plotHaps.md) | **plotHaps** provides the formatted output that can be used with 'bin/plotHaplotypes.R'. |
 | [vcfsitesummarize](https://github.com/vcflib/vcflib/blob/master/doc/vcfsitesummarize.md) | Summarize by site |
 | [vcfgenotypecompare](https://github.com/vcflib/vcflib/blob/master/doc/vcfgenotypecompare.md) | adds statistics to the INFO field of the vcf file describing the amount of discrepancy between the genotypes (GT) in the vcf file and the genotypes reported in the <other-genotype-tag>. use this after vcfannotategenotypes to get correspondence statistics for two vcfs. |
 | [vcfstats](https://github.com/vcflib/vcflib/blob/master/doc/vcfstats.md) | Prints statistics about variants in the input VCF file. |
 | [wcFst](https://github.com/vcflib/vcflib/blob/master/doc/wcFst.md) | **wcFst** is Weir & Cockerham's Fst for two populations. Negative values are VALID, they are sites which can be treated as zero Fst. For more information see Evolution, Vol. 38 N. 6 Nov 1984. Specifically **wcFst** uses equations 1,2,3,4. |
 | [permuteSmooth](https://github.com/vcflib/vcflib/blob/master/doc/permuteSmooth.md) | **permuteSmooth** is a method for adding empirical p-values smoothed wcFst scores. |
 | [bFst](https://github.com/vcflib/vcflib/blob/master/doc/bFst.md) | **bFst** is a Bayesian approach to Fst. Importantly **bFst** accounts for genotype uncertainty in the model using genotype likelihoods. For a more detailed description see: `A Bayesian approach to inferring population structure from dominant markers' by Holsinger et al. Molecular Ecology Vol 11, issue 7 2002. The likelihood function has been modified to use genotype likelihoods provided by variant callers. There are five free parameters estimated in the model: each subpopulation's allele frequency and Fis (fixation index, within each subpopulation), a free parameter for the total population's allele frequency, and Fst. |
 | [vcfroc](https://github.com/vcflib/vcflib/blob/master/doc/vcfroc.md) | Generates a pseudo-ROC curve using sensitivity and specificity estimated against a putative truth set. Thresholding is provided by successive QUAL cutoffs. |
 | [vcfparsealts](https://github.com/vcflib/vcflib/blob/master/doc/vcfparsealts.md) | Alternate allele parsing method. This method uses pairwise alignment of REF and ALTs to determine component allelic primitives for each alternate allele. |
 | [pFst](https://github.com/vcflib/vcflib/blob/master/doc/pFst.md) | **pFst** is a probabilistic approach for detecting differences in allele frequencies between two populations. |
 | [iHS](https://github.com/vcflib/vcflib/blob/master/doc/iHS.md) | **iHS** calculates the integrated haplotype score which measures the relative decay of extended haplotype homozygosity (EHH) for the reference and alternative alleles at a site (see: voight et al. 2006, Spiech & Hernandez 2014). |
 | [popStats](https://github.com/vcflib/vcflib/blob/master/doc/popStats.md) | General population genetic statistics for each SNP |

See also [vcflib.md](https://github.com/vcflib/vcflib/blob/master/doc/vcflib.md).

#### scripts

The vcflib source repository contains a number of additional scripts.
Click on the link to see the source code.

| script | description |
| :-------------- | :---------- |
| [vcfclearinfo](https://github.com/vcflib/vcflib/blob/master/scripts/vcfclearinfo) | clear INFO field |
| [vcfqualfilter](https://github.com/vcflib/vcflib/blob/master/scripts/vcfqualfilter) | quality filter |
| [vcfnulldotslashdot](https://github.com/vcflib/vcflib/blob/master/scripts/vcfnulldotslashdot) | rewrite null genotypes to https://github.com/vcflib/vcflib/blob/master/. |
| [vcfprintaltdiscrepancy.r](https://github.com/vcflib/vcflib/blob/master/scripts/vcfprintaltdiscrepancy.r) | show ALT discrepancies in a table |
| [vcfremovenonATGC](https://github.com/vcflib/vcflib/blob/master/scripts/vcfremovenonATGC) | remove non-nucleotides in REF or ALT |
| [plotSmoothed.R](https://github.com/vcflib/vcflib/blob/master/scripts/plotSmoothed.R) | smooth plot of wcFst, pFst or abba-baba |
| [vcf_strip_extra_headers](https://github.com/vcflib/vcflib/blob/master/scripts/vcf_strip_extra_headers) | strip headers |
| [plotHapLrt.R](https://github.com/vcflib/vcflib/blob/master/scripts/plotHapLrt.R) | plot results of pFst |
| [vcfbiallelic](https://github.com/vcflib/vcflib/blob/master/scripts/vcfbiallelic) | remove anything that is not biallelic |
| [vcfsort](https://github.com/vcflib/vcflib/blob/master/scripts/vcfsort) | sort VCF using shell script |
| [vcfnosnps](https://github.com/vcflib/vcflib/blob/master/scripts/vcfnosnps) | remove SNPs |
| [vcfmultiwayscripts](https://github.com/vcflib/vcflib/blob/master/scripts/vcfmultiwayscripts) | more multiway comparisons |
| [vcfgtcompare.sh](https://github.com/vcflib/vcflib/blob/master/scripts/vcfgtcompare.sh) | annotates records in the first file with genotypes and sites from the second |
| [plotPfst.R](https://github.com/vcflib/vcflib/blob/master/scripts/plotPfst.R) | plot pFst |
| [vcfregionreduce_and_cut](https://github.com/vcflib/vcflib/blob/master/scripts/vcfregionreduce_and_cut) | reduce, gzip, and tabix |
| [plotBfst.R](https://github.com/vcflib/vcflib/blob/master/scripts/plotBfst.R) | plot results of pFst |
| [vcfnobiallelicsnps](https://github.com/vcflib/vcflib/blob/master/scripts/vcfnobiallelicsnps) | remove biallelic SNPs |
| [vcfindels](https://github.com/vcflib/vcflib/blob/master/scripts/vcfindels) | show INDELS |
| [vcfmultiway](https://github.com/vcflib/vcflib/blob/master/scripts/vcfmultiway) | multiway comparison |
| [vcfregionreduce](https://github.com/vcflib/vcflib/blob/master/scripts/vcfregionreduce) | reduce VCFs using a BED File, gzip them up and create tabix index |
| [vcfprintaltdiscrepancy.sh](https://github.com/vcflib/vcflib/blob/master/scripts/vcfprintaltdiscrepancy.sh) | runner |
| [vcfclearid](https://github.com/vcflib/vcflib/blob/master/scripts/vcfclearid) | clear ID field |
| [vcfcomplex](https://github.com/vcflib/vcflib/blob/master/scripts/vcfcomplex) | remove all SNPs but keep SVs |
| [vcffirstheader](https://github.com/vcflib/vcflib/blob/master/scripts/vcffirstheader) | show first header |
| [plotXPEHH.R](https://github.com/vcflib/vcflib/blob/master/scripts/plotXPEHH.R) | plot XPEHH |
| [vcfregionreduce_pipe](https://github.com/vcflib/vcflib/blob/master/scripts/vcfregionreduce_pipe) | reduce, gzip and tabix in a pipe |
| [vcfplotaltdiscrepancy.sh](https://github.com/vcflib/vcflib/blob/master/scripts/vcfplotaltdiscrepancy.sh) | plot ALT discrepancy runner |
| [vcfplottstv.sh](https://github.com/vcflib/vcflib/blob/master/scripts/vcfplottstv.sh) | runner |
| [vcfnoindels](https://github.com/vcflib/vcflib/blob/master/scripts/vcfnoindels) | remove INDELs |
| [bgziptabix](https://github.com/vcflib/vcflib/blob/master/scripts/bgziptabix) | runs bgzip on the input and tabix indexes the result |
| [plotHaplotypes.R](https://github.com/vcflib/vcflib/blob/master/scripts/plotHaplotypes.R) | plot results |
| [vcfplotsitediscrepancy.r](https://github.com/vcflib/vcflib/blob/master/scripts/vcfplotsitediscrepancy.r) | plot site discrepancy |
| [vcfindelproximity](https://github.com/vcflib/vcflib/blob/master/scripts/vcfindelproximity) | show SNPs around an INDEL |
| [bed2region](https://github.com/vcflib/vcflib/blob/master/scripts/bed2region) | convert VCF CHROM column in VCF file to region |
| [vcfplotaltdiscrepancy.r](https://github.com/vcflib/vcflib/blob/master/scripts/vcfplotaltdiscrepancy.r) | plot ALT discrepancies |
| [plot_roc.r](https://github.com/vcflib/vcflib/blob/master/scripts/plot_roc.r) | plot ROC |
| [vcfmultiallelic](https://github.com/vcflib/vcflib/blob/master/scripts/vcfmultiallelic) | remove anything that is not multiallelic |
| [vcfsnps](https://github.com/vcflib/vcflib/blob/master/scripts/vcfsnps) | show SNPs |
| [vcfvarstats](https://github.com/vcflib/vcflib/blob/master/scripts/vcfvarstats) | use fastahack to get stats |
| [vcfregionreduce_uncompressed](https://github.com/vcflib/vcflib/blob/master/scripts/vcfregionreduce_uncompressed) | reduce, gzip and tabix |
| [plotWCfst.R](https://github.com/vcflib/vcflib/blob/master/scripts/plotWCfst.R) | plot wcFst |
| [vcf2bed.py](https://github.com/vcflib/vcflib/blob/master/scripts/vcf2bed.py) | transform VCF to BED file |
| [vcfjoincalls](https://github.com/vcflib/vcflib/blob/master/scripts/vcfjoincalls) | overlay files using QUAL and GT from a second VCF |
| [vcf2sqlite.py](https://github.com/vcflib/vcflib/blob/master/scripts/vcf2sqlite.py) | push VCF file into SQLite3 database using dbname |

In order to use this image you need to run the folliwing command: `docker run --rm -v /your/data/dir:/data bioinfoipec/vcflib <tool-option>`

See the [`MANUAL`](https://github.com/vcflib/vcflib), for more details.

To obtain help of an tool usage, you just need to run: `docker run --rm bioinfoipec/vcflib <tol-option> -h`.

## Test data
To test the previous command, you can access the [following link](https://github.com/vcflib/vcflib).