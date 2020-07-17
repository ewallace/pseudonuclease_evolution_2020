# pseudonuclease_evolution_2020/data/BLASTp

Data relating to BLASTp search for Dis3L2 homologs in select eukaryotes.

## curated_76species_taxid.txt

List of 76 species with NCBI taxon id, that we searched for Dis3L2 homologs.

## BLASTp_hittable_76species_BBWCMDV1016.txt

BLASTp hit table from searching those species for homologs of each of:

* Q8IYB7.4 - Homo Sapiens Dis3L2, HsDis3L2
* P24276.1 - Saccharomyces cerevisiae SSD1, ScSsd1
* O14040.1 - Schizosaccharomyces pombe Dis3L2, SpDis3L2

## HsDis3L2_BLASTp_76species_fullseqs.fasta

Full protein sequences in fasta format for HsDis3L2 BLASTp hits.

## ScSsd1_BLASTp_76species_fullseqs.fasta

Full protein sequences in fasta format for ScSsd1 BLASTp hits.

## SpDis3L2_BLASTp_76species_fullseqs.fasta

Full protein sequences in fasta format for SpDis3L2 BLASTp hits.

## Ssd1Dis3L2_BLASTp_76species_filteredbyhand_fullseqs.fasta

Unique full protein sequences from BLASTp hits above, filtered:

* E-value < 1
* alignment length at least 200
* truncated sequences removed (done "by hand" by EW, by inspecting a MAFFT alignment and fasttree analysis of these sequences)

## Ssd1Dis3L2_BLASTp_76species_filteredbyhand_fullseqs_mafft_trimalstrong.fasta

This is a trimmed multiple sequence alignment of sequences in the above file, produced by running the code:

```
mafft --retree 2 --reorder "BLASTs_8May2020/Ssd1Dis3L2_BLASTp_76species_filteredbyhand_fullseqs.fasta" > "BLASTs_8May2020/Ssd1Dis3L2_BLASTp_76species_filteredbyhand_fullseqs_mafft.fasta"

trimal -gt 0.25 -resoverlap 0.75 -seqoverlap 75 -in "BLASTs_8May2020/Ssd1Dis3L2_BLASTp_76species_filteredbyhand_fullseqs_mafft.fasta" -out "BLASTs_8May2020/Ssd1Dis3L2_BLASTp_76species_filteredbyhand_fullseqs_mafft_trimalstrong.fasta"
```

Note that the intermediate file,
`BLASTs_8May2020/Ssd1Dis3L2_BLASTp_76species_filteredbyhand_fullseqs_mafft.fasta`,
is not included in this repository as it should be able to recreated it as above.

Software versions and references are:

* MAFFT v7.429, (Katoh, Kazutaka, and Daron M Standley. 2013. “MAFFT Multiple Sequence Alignment Software Version 7: Improvements in Performance and Usability.” Molecular Biology and Evolution 30 (4): 772–80. https://doi.org/10.1093/molbev/mst010.)
* trimAl v1.4.rev15  (Capella-Gutiérrez, Salvador, José M Silla-Martínez, and Toni Gabaldón. 2009. “trimAl: A Tool for Automated Alignment Trimming in Large-Scale Phylogenetic Analyses.” Bioinformatics (Oxford, England) 25 (15): 1972–3. https://doi.org/10.1093/bioinformatics/btp348.)
