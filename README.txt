This archive contains the core analysis scripts for the Senegal sorghum
hyperspectral GWAS study.

1) sorghum_spectral_main.py
   - Builds the seed phenome + spectral matrices
   - Constructs genotype matrices and PCs
   - Computes spectral heritability and genetic–spectral distance
   - Runs main spectral GWAS, path analysis, in-silico simulations
   - Annotates GWAS hits with sorghum gene models

2) sorghum_interseed_postgwas.py
   - Post-GWAS processing for inter-seed distribution traits
   - Calls Bonferroni-significant QTLs from GEMMA outputs
   - Maps QTLs to candidate genes using the main gene summary
   - Enriches gene descriptions using Phytozome defline files

Input files and directory layout follow the Methods and
Supplementary Data S1 of the manuscript.
