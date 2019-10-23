Here are answers to frequently asked questions about datasets generated in the Balasubramanian group:

- **G-quadruplexes**:
  - [Observed DNA G-quadruplex sequences in the human genome](README.md#observed-dna-g-quadruplex-sequences-in-the-human-genome)
  - [Observed DNA G-quadruplex sequences in multiple species](README.md#observed-dna-g-quadruplex-sequences-in-multiple-species)
  - [Observed RNA G-quadruplex sequences in the human transcriptome](README.md#observed-rna-g-quadruplex-sequences-in-the-human-transcriptome)
  - [Which DNA G-quadruplex dataset was used to train the software Quadron](README.md#observed-dna-g-quadruplex-sequences-in-the-human-genome)

- **Modified bases**:
  - [Genome-wide mapping of 5hmU and base J in Leishmania](README.md#genome-wide-mapping-of-5hmu-and-base-j-in-Leishmania)


## Observed DNA G-quadruplex sequences in the human genome

The DNA G-quadruplex annotation of the human genome as presented in [Chambers et *al.*, 2015](https://www.nature.com/articles/nbt.3295) is available in GEO [GSE63874](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE63874) - see Supplementary files.

The files to use are the observed G-quadruplex sequences in common to the 2 K+ experiments as detected on the forward and reverse strands respectively with coordinates from the human hg19 reference genome:

- GSE63874_Na_K_minus_hits_intersect.bed.gz
- GSE63874_Na_K_plus_hits_intersect.bed.gz

The formatting of these files is:

- 1st column: chromosome
- 2nd column: start of the observed G-quadruplex
- 3rd column: end of the observed G-quadruplex

You can use [bedtools](https://bedtools.readthedocs.io/en/latest/) if you'd like to merge the two files above using the following command:

```
bedtools merge -i <(zcat GSE63874_Na_K_* | bedtools sort -i) > GSE63874_Na_K.bed
```

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



## Observed DNA G-quadruplex sequences in multiple species

The DNA G-quadruplex annotation in multiple species as presented in [Marsico et *al.*, 2019](https://academic.oup.com/nar/article/47/8/3862/5403498) is available in GEO [GSE110582](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE110582).

Go to the Samples section and find your species of interest and the condition used in the experiment, e.g. Homo sampiens and K+ experiment Homo_Li_K [GSM3003539](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM3003539). The files to use are `*.hits.max.K.w50.25.bed.gz`. The formatting of these files is:

- 1st column: chromosome
- 2nd column: start of the observed G-quadruplex
- 3rd column: end of the observed G-quadruplex
- 4th column: score



## Observed RNA G-quadruplex sequences in the human transcriptome

The RNA G-quadruplex annotation of the human transcriptome as presented in [Kwok et *al.*, 2016](https://www.nature.com/articles/nmeth.3965) is available in GEO [GSE77282](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE77282).

Scroll down to the Supplementary files section. The file to use is `GSE77282_K_hits.bed.gz`.



## Genome-wide mapping of 5hmU and base J in Leishmania

The 5hmU maps in the Leishmania donovani and Leishmania major genomes as presented in [Kawasaki et *al.*, 2017](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-017-1150-1) are available in GEO [GSE83384](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE83384).

Go to the Samples section and find your species of interest (Lmaj - major, Ldon - donovani) and the methodology used to map 5hmU (DIP, chem) or J, e.g. L. major chmemical enrichment rep 1 fk050_Lmaj_chem1 [GSM2200481](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM2200481). The file to use ends with `*.peaks.txt.gz`.

