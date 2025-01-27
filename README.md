

# HSC scRNA-ATAC-seq Analysis

This repository contains the analysis and results of a single-cell multi-omics study combining scRNA-seq and ATAC-seq data to investigate hematopoietic stem cells (HSCs) across different age groups. The analysis focuses on the transcriptional and chromatin accessibility landscapes in young and aged HSCs.

---

## Data Source
The data used for this analysis is publicly available on GEO under the accession [GSE190424](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE190424). The study provides high-resolution single-cell datasets, allowing detailed insights into HSC biology. 


## Analysis Overview

### Objective
The study aims to:
1. Compare gene expression profiles between young and aged HSCs.
2. Identify chromatin accessibility differences linked to aging.
3. Integrate scRNA-seq and ATAC-seq datasets for a comprehensive understanding of age-related changes.

### Data Preprocessing
The following datasets were used:
- **scRNA-seq Data**: Preprocessed into filtered gene-barcode matrices.
- **ATAC-seq Data**: Preprocessed into peak-barcode matrices and fragment files.

### Methods
- **Dimensionality Reduction**: PCA and UMAP were applied to reduce data dimensions while preserving biological variance.
- **Clustering**: Louvain clustering was performed to identify distinct cell populations.
- **Integration**: Matrices from scRNA-seq and ATAC-seq were integrated using Seurat and ArchR to assess correlations between chromatin accessibility and gene expression.

The detailed analysis pipeline is available in the RMarkdown script: `scripts/HSC_scRNA-ATAC_seq.Rmd`.



---

## Results

### 1. Transcriptional Profiles
- **Key Finding**: Aged HSCs exhibited altered expression of genes associated with stemness (e.g., _GATA2_, _RUNX1_) and differentiation.
- **Visualization**: Violin plots highlighted increased variability in gene expression levels for differentiation-related markers in aged HSCs.

### 2. Chromatin Accessibility
- **Key Finding**: Aged HSCs displayed reduced accessibility in promoter and enhancer regions of stemness-related genes.
- **Visualization**: Coverage plots demonstrated decreased chromatin accessibility at loci for _GATA2_ and _MYC_ in aged cells.

### 3. Integrated Analysis
- **Key Finding**: Strong correlation between chromatin accessibility and gene expression changes in aged HSCs.
- **Visualization**: Feature plots overlaid chromatin and gene expression signals, showing a decline in regions critical for self-renewal in aged HSCs.
