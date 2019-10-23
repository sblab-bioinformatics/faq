Here are answers to frequently asked questions about resources from the group:

- G-quadruplexes:
  - [Observed G-quadruplex sequences](README.md#observed-g-quadruplex-sequences)

- Modified bases:


## Observed G-quadruplex sequences

The G-quadruplex annotation of the human genome as presented in [Chambers et **al.**, 2015](https://www.nature.com/articles/nbt.3295) is available in GEO [GSE63874](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE63874) - see Supplementary files.

The files to use are the observed G-quadruplex sequences in common to the 2 K+ experiments as detected on the forward and reverse strands respectively with coordinates from the human hg19 reference genome:

- GSE63874_Na_K_minus_hits_intersect.bed.gz
- GSE63874_Na_K_plus_hits_intersect.bed.gz

The formatting of these files is:

- 1st column: chromosome
- 2nd column: start of the observed G-quadruplex
- 3rd column: end of the observed G-quadruplex

You can use [bedtools](https://bedtools.readthedocs.io/en/latest/) if you'd like to merge the two files above using the following command:

bedtools merge -i <(zcat GSE63874_Na_K_* | bedtools sort -i) > GSE63874_Na_K.bed

These files and others are publicly available to download from GEO in the following link:

https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE63874

for more details about each individual file type and design, please read this:

ftp://ftp.ncbi.nlm.nih.gov/geo/series/GSE63nnn/GSE63874/suppl/GSE63874%5FREADME%2Etxt


