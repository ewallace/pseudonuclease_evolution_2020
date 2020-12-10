[![DOI](https://zenodo.org/badge/280423586.svg)](https://zenodo.org/badge/latestdoi/280423586)

# pseudonuclease_evolution_2020

Evolutionary analysis of Dis3/RNase II-family enzymes, including the fungal Ssd1 pseudonuclease.

This repository forms the supplementary data and analysis for the manuscript:

*Repeated evolution of inactive pseudonucleases in a fungal branch of the Dis3/RNase II family of nucleases*; 
E.R. Ballou, A.G. Cook, E.W.J. Wallace. Molecular Biology and Evolution, 2020.
DOI: [10.1093/molbev/msaa324](http://dx.doi.org/10.1093/molbev/msaa324)

Every directory has a README.md that describes the contents in more detail.

# License

Original code and data analysis in the repository is covered by an Apache 2.0 licence, see LICENCE.

Data copied from other sources are covered by more permissive licences.
For example, sequence data and ids, taxonomic info, and BLAST results from the US National Library of Medicine.
Webpage results (e.g. BLAST) are public-domain, see https://www.ncbi.nlm.nih.gov/home/about/policies/#copyright for more details. 

## data

Data files, both input and output data.

Some analyses are described in relevant logfiles and READMEs in subdirectories of data: 

* multiple sequence alignment (MAFFT)
* alignment processing (TrimAl)
* phylogenetic analysis (IQ-TREE)

## src

Scripts in R markdown format that do the rest of the data processing and analysis, including making figures used in the manuscript.


## figure

Figures used in the manuscript, output by scripts in src
