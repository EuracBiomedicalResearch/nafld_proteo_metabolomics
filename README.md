# MASLD omics data analyses

This repository contains data processing and association analyses for the CHRIS
NAFLD (MASLD) data resources.

## General data analysis

- General data overview and definition of the MASLD phenotypes:
  [nafld_data_overview.Rmd](nafld_data_overview.Rmd)

## Data processing/preprocessing

- Preprocessing of the NAFLD/MASLD untargeted metabolomics data set (positive
  polarity) [NAFLD_Prepro_pos.Rmd](NAFLD_Prepro_pos.Rmd).

## Association analyses

Association analyses were already performed, but need to be re-performed with
the proper phenotypes defines in the *General data analysis*.
- Linear models of the NAFLD/MASLD targeted metabolomics data set 
  [NAFLD_metab_targeted_lm.Rmd](NAFLD_metab_targeted_lm.Rmd).

## Required packages and setup

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
