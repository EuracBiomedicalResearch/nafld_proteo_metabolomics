# MASLD omics data analyses

This repository contains data processing and association analyses for the CHRIS
NAFLD (MASLD) data resources.

## General data analysis

- General data overview and definition of the MASLD phenotypes:
  [nafld_data_overview.Rmd](nafld_data_overview.Rmd)

## Data processing/preprocessing

- Preprocessing of the NAFLD/MASLD untargeted metabolomics data set (positive
  polarity) [NAFLD_Prepro_pos.Rmd](NAFLD_Prepro_pos.Rmd).
- Normalisation of the NAFLD/MASLD untargeted metabolomics data set (positive
  polarity) [NAFLD_Norm_pos.Rmd](NAFLD_Norm_pos.Rmd).

## Association analyses

- Association analysis of scanningswath proteomics, targeted metabolomics and
  dietary intake for liver steatosis:
  [NAFLD_steatosis_associations.Rmd](NAFLD_steatosis_associations.Rmd). This is
  the current **main** analysis.
- Investigation of the confounding effect of PDI on the association analysis of
  scanningswath proteomics and targeted metabolomics for liver steatosis:
  [NAFLD_steatosis_foodindex_influence.Rmd](NAFLD_steatosis_foodindex_influence.Rmd).
- Association analysis of scanningswath proteomics and targeted metabolomics for
  liver fibrosis:
  [mNAFLD_fibrosis_explore.Rmd](NAFLD_fibrosis_explore.Rmd)
- Association analysis of scanningswath proteomics and targeted metabolomics for
  MASH:
  [NAFLD_MASH_and_tables.Rmd](NAFLD_MASH_and_tables.Rmd)
- Association analysis of untargeted metabolomics for liver steatosis:
  [NAFLD_metab_untargeted_pos_lm.Rmd](NAFLD_metab_untargeted_pos_lm.Rmd)

## Pathway analysis

- Pathway analysis using Ramp-DB of scanningswath proteomics and targeted
  metabolomics was performed online, so no script is available.
- Pathway analysis using Mummichog algorithm of untargeted metabolomics for
  liver steatosis:
  [NAFLD_naab13_mumichog.Rmd](NAFLD_naab13_mumichog.Rmd)

## Preliminary analyses

- Preliminary exploratory analysis of the NAFLD CHRIS sub-study scanningswath
  proteomics data:
  [NAFLD_scanningswath_proteomics_exploratory_analysis.Rmd](NAFLD_scanningswath_proteomics_exploratory_analysis.Rmd)
- Analysis to identify Scanning SWATH proteins that are related to liver
  stiffness, FIB4 variable and liver fat:
  [NAFLD_related_proteins.Rmd](NAFLD_related_proteins.Rmd)
- Preliminary exploratory analysis of the NAFLD CHRIS sub-study targeted
  metabolomics data:
  [NAFLD_metabolomics_exploratory_analysis.Rmd](NAFLD_scanningswath_proteomics_exploratory_analysis.Rmd)
- Analysis to identify targeted metabolites that are related to liver stiffness,
  FIB4 variable and liver fat:
  [NAFLD_related_metabolites.Rmd](NAFLD_related_metabolites.Rmd)
- Comparison between the NAFLD participants metabolomics and proteomics
  measurements in the CHRIS baseline and NAFLD CHRIS sub-study:
  [comparison_nafld_baseline_omics.Rmd](comparison_nafld_baseline_omics.Rmd)
- Compilation of the NAFLD CHRIS sub-study untargeted metabolomics data set:
  [nalfd_untargeted_metabolomics_dataset.Rmd](nalfd_untargeted_metabolomics_dataset.Rmd)


# Required packages and setup

The analysis requires a recent version of R (version >= 3.6.0) and a set of R
packages that can be installed with the code below.

```r
install.packages("BiocManager")
library(BiocManager)
BiocManager::install(c("BiocStyle",
                       "xcms",
                       "RColorBrewer",
                       "pander",
                       "UpSetR",
                       "pheatmap",
                       "SummarizedExperiment",
                       "MsExperiment",
                       "Spectra",
                       "MetaboCoreUtils",
                       "MsBackendSql",
                       "MsQuality",
                       "writexl",
                       "ProtGenerics",
                       "MsCoreUtils",
                       "MetaboAnnotation"))

install.packages(c("tidyverse",
                   "readxl",
                   "readr",
                   "RSQLite",
                   "rmarkdown",
                   "kableExtra",
                   "magick",
                   "vioplot",
                   "pandoc",
                   "pander",
                   "car",
                   "DT",
                   "ggfortify",
                   "ggplot2",
                   "ggpubr",
                   "reshape2",
                   "plotly",
                   "rgl",
                   "writexl"))

remotes::install_github("EuracBiomedicalResearch/tidyfr")



```
