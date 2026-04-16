# Sorghum Seed Spectral Manifold

This repository contains the analysis workflow used for downstream spectral, morphology, GWAS, and inter-seed heterogeneity analyses in Senegalese sorghum seeds.

## Repository layout

- `main/sorghum_spectral_main.py`
  - Core manuscript analysis pipeline
  - Builds spectral summary matrices from processed inputs
  - Merges morphology and spectral traits
  - Constructs genotype PCs
  - Prepares GEMMA inputs and summarizes GWAS/QTL results
  - Runs path analysis and in silico manifold perturbation
  - Annotates GWAS summaries with sorghum gene models

- `main/sorghum_interseed_postgwas.py`
  - Post-GWAS processing for inter-seed optical heterogeneity traits
  - Summarizes QTLs from GEMMA association outputs
  - Maps intervals to candidate genes
  - Enriches descriptions with annotation resources

- `support/support_tables.py`
  - Additional downstream summary analyses (tables only; no figure generation)
  - Computes empirical LD decay, genotype PCA scree, chromosome 6 local summaries,
    locus-level peak tables, and related summary outputs

- `support/support_core.py`
  - Shared utilities for the downstream summary analyses

## What is not included

- Figure-generation or figure-refinement scripts used only for manuscript layout
- Exploratory or troubleshooting notebooks
- Raw hyperspectral image cubes
- Platform-specific executables (for example, PLINK or GEMMA binaries)

## Data sources expected by this repository

Please see `docs/input_data_sources.md` for the full list. In brief:

- Seed morphology phenotype data: previously published supplementary data
- SNP genotype data: public Figshare repository
- Curated spectral and GWAS summary tables: Supplementary Data S1 of the manuscript
- Raw hyperspectral image data: available from the corresponding author upon reasonable request

## External tools

This repository does not bundle GEMMA or PLINK.

- The core manuscript script prepares GEMMA input files and summarizes outputs after external GEMMA execution.
- The additional summary script works directly from curated project files and existing GWAS outputs; PLINK is not required for normal downstream reruns.

## Quick start

See `run_examples.txt` for platform-specific example commands that can be adapted to your local project layout.

## Notes

This repository focuses on reproducible downstream analyses from processed inputs. It is intended for rerunning manuscript-level analyses from curated data products rather than rebuilding the workflow from raw hyperspectral image cubes.
