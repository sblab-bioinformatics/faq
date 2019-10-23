Here are answers to frequently asked questions about resources from the group:

- **G-quadruplexes**:
  - [Observed G-quadruplex sequences in the human genome](README.md#observed-g-quadruplex-sequences-in-the-human-genome)
  - [Observed G-quadruplex sequences in multiple species](README.md#observed-g-quadruplex-sequences-in-multiple-species)
  - [Which G-quadruplex dataset was used to train the software Quadron](README.md#observed-g-quadruplex-sequences-in-the-human-genome)

- **Modified bases**:


## Observed G-quadruplex sequences in the human genome

The G-quadruplex annotation of the human genome as presented in [Chambers et *al.*, 2015](https://www.nature.com/articles/nbt.3295) is available in GEO [GSE63874](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE63874) - see Supplementary files.

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

A more recently updated map of observed G-quadruplex sequences in the human genome is available in GEO [GSE110582](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE110582). Go to the Samples section and select Homo_Li_K [GSM3003539](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM3003539). The files to use are the correspond to the K+ experiments as detected on the forward and reverse strands respectively with coordinates from the human hg19 reference genome:

- GSM3003539_Homo_all_w15_th-1_minus.hits.max.K.w50.25.bed.gz
- GSM3003539_Homo_all_w15_th-1_plus.hits.max.K.w50.25.bed.gz

The formatting of these files is:

- 1st column: chromosome
- 2nd column: start of the observed G-quadruplex
- 3rd column: end of the observed G-quadruplex
- 4th column: score



## Observed G-quadruplex sequences in multiple species

The G-quadruplex annotation in multiple as presented in [Marsico et *al.*, 2019](https://academic.oup.com/nar/article/47/8/3862/5403498) is available in GEO [GSE110582](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE110582).

Go to the Samples section and find your species of interest and the condition used in the experiment, e.g. Homo sampiens and K+ experiment Homo_Li_K [GSM3003539](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM3003539). The files to use are `*.hits.max.K.w50.25.bed.gz`. The formatting of these files is:

- 1st column: chromosome
- 2nd column: start of the observed G-quadruplex
- 3rd column: end of the observed G-quadruplex
- 4th column: score
