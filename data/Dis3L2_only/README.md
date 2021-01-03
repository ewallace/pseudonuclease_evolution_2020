# pseudonuclease_evolution_2020/data/Dis3L2_only

Data on Dis3L2-specific homologs, including S. cerevisiae Ssd1, in select eukaryotes.
This data follows on from the sequences in `data/Dis3_families/Dis3L2_BLASTp_select_fullseqs.fasta`.

## Dis3L2_BLASTp_select_fullseqs_mafftlocal_trimal.fasta

This is a trimmed multiple sequence alignment of sequences in the above file, produced by running the code:

```
mafft --thread 4 --localpair --maxiterate 1000 --retree 2 --reorder  "data/Dis3_families/Dis3L2_BLASTp_select_fullseqs.fasta" > "data/Dis3L2_only/Dis3L2_BLASTp_select_fullseqs_mafftlocal.fasta"

trimal -gt 0.25 -resoverlap 0.75 -seqoverlap 75 -in "data/Dis3L2_only/Dis3L2_BLASTp_select_fullseqs_mafftlocal.fasta" -out "data/Dis3L2_only/Dis3L2_BLASTp_select_fullseqs_mafftlocal_trimal.fasta"
```

The intermediate file,
`data/Dis3L2_only/Dis3L2_BLASTp_select_fullseqs_mafftlocal.fasta`,
is also included in this repository. It is used as input for feature calculation 

Software versions and references are:

* MAFFT v7.429, (Katoh, Kazutaka, and Daron M Standley. 2013. “MAFFT Multiple Sequence Alignment Software Version 7: Improvements in Performance and Usability.” Molecular Biology and Evolution 30 (4): 772–80. https://doi.org/10.1093/molbev/mst010.)
* trimAl v1.4.rev15  (Capella-Gutiérrez, Salvador, José M Silla-Martínez, and Toni Gabaldón. 2009. “trimAl: A Tool for Automated Alignment Trimming in Large-Scale Phylogenetic Analyses.” Bioinformatics (Oxford, England) 25 (15): 1972–3. https://doi.org/10.1093/bioinformatics/btp348.)

## N-terminal and delta N-terminal

* Dis3L2_BLASTp_select_fullseqs_mafftlocal_trimal_deltaNterm1to337.fasta
* Dis3L2_BLASTp_select_fullseqs_mafftlocal_trimal_Nterm1to337.fasta

These was created from `Dis3L2_BLASTp_select_fullseqs_mafftlocal_trimal.fasta` by EW inspecting the sequence and deleting/selecting the Nterminal segment aligned to S. cerevisiae Ssd1 residues 1-337, in Aliview.

The `..._deltaNterm1to337.fasta` file is used as input to IQ-TREE alignment calculation.

The `..._Nterm1to337.fasta` files is used for some feature calculations.

## Dis3L2_BLASTp_select_taxa.txt

Taxonomic information for Dis3L2/Ssd1 homologs.
Table with taxonomic information, separated out from fasta headers.

## Dis3L2_BLASTp_select_features.txt

Information and features of Dis3L2/Ssd1 homologs 
calculated from Dis3L2_BLASTp_select_fullseqs_mafftlocal.fasta, etc.
taxonomic info, active site, cbk1 consensus phosphorylation site, cdk1 sites, nuclear localisation sequence.
See `src/estimate_features_Dis3L2_only.Rmd` for full descriptions and code
