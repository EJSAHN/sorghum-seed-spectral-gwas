# Input data sources

## Seed morphology phenotype data

Previously published supplementary data:

- Ahn E. et al. Genome-wide association study of seed morphology traits in Senegalese sorghum cultivars. *Plants* 12, 2344 (2023).
- Supplementary Data S1 at the Plants article.

## SNP genotype data

Public repository:

- Figshare DOI: https://doi.org/10.6084/m9.figshare.30877697
- Landing page: https://figshare.com/articles/dataset/_b_Genotypic_Data_SNPs_for_Sorghum_Mini_Core_Collection_and_Senegalese_Accessions_b_/30877697

## Curated manuscript-level tables

Expected local project files:

- Seed phenome tables such as `seed_phenome_master*.csv`
- Supplementary Data S1 associated with the spectral-manifold manuscript
- GEMMA association outputs (`*.assoc.txt`)
- Gene annotation resources (`*.gff3`, annotation info, defline, synonym tables)

## Raw hyperspectral data

Raw hyperspectral image cubes are not bundled here. This repository is designed to rerun downstream analyses from curated phenotype/genotype inputs and GWAS summary files.

## External software

- GEMMA: required externally for association scans if users wish to regenerate GWAS outputs from prepared inputs
- PLINK: not required for normal downstream reruns of the shared analysis workflow
