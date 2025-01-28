# HSC scRNA-ATAC-seq Analysis

This repository contains the analysis and results of a single-cell multi-omics study combining **scRNA-seq** and **ATAC-seq** data to investigate **hematopoietic stem cells (HSCs)** across different age groups. The analysis focuses on the transcriptional and chromatin accessibility landscapes in **young and aged HSCs**, with a particular emphasis on age-related changes in chromatin accessibility and stress response pathways.

This work is a reproduction of the research presented in the paper:  
**"Epigenetic traits inscribed in chromatin accessibility in aged hematopoietic stem cells"** by Itokawa et al., published in *Nature Communications* (2022).  
[DOI: 10.1038/s41467-022-30374-9](https://doi.org/10.1038/s41467-022-30374-9) | [PMID: 35577813](https://pubmed.ncbi.nlm.nih.gov/35577813/)

---

## Data Source
The data used for this analysis is publicly available on **GEO** under the accession [GSE190424](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE190424). The study provides high-resolution single-cell datasets, allowing detailed insights into HSC biology.

---

## Analysis Overview

### Objective
The study aims to:
1. Compare gene expression profiles between **young and aged HSCs**.
2. Identify **chromatin accessibility differences** linked to aging.
3. Integrate **scRNA-seq** and **ATAC-seq** datasets to understand age-related changes in gene regulation and stress responses.

### Key Findings from the Paper
- **Chromatin Accessibility Changes**: Aged HSCs exhibit alterations in chromatin accessibility, particularly in regions enriched for **STAT, ATF, and CNC family transcription factor motifs**.
- **Stress Response Pathways**: Open differentially accessible regions (open DARs) in aged HSCs are linked to **augmented transcriptional responses** under stress conditions.
- **Enhancer States**: Most open DARs comprise **active, primed, and inactive enhancers**, suggesting a role in regulating stress-induced gene expression.


---

## Workflow

### 1. Data Preprocessing
- **scRNA-seq Data**: Preprocessed into filtered gene-barcode matrices.
- **ATAC-seq Data**: Preprocessed into peak-barcode matrices and fragment files.

### 2. Identification of Open DARs
- Differentially open accessible regions (open DARs) were identified using peak calling and differential accessibility analysis.
- Motif enrichment analysis was performed to identify transcription factor binding sites (e.g., **STAT, ATF, CNC family**).

### 3. Integration of scRNA-seq and ATAC-seq Data
- Matrices from scRNA-seq and ATAC-seq were integrated using **Seurat** and **ArchR**.
- Correlation analysis was performed to link chromatin accessibility changes with gene expression changes.

### 4. Stress Response Analysis
- Basal and cytokine-stimulated gene expression levels were compared between young and aged HSCs.
- Open DARs were linked to genes showing **augmented transcriptional responses** under stress conditions.

---

## Results

### 1. Transcriptional Profiles
- Aged HSCs exhibited altered expression of genes associated with **stemness (e.g., GATA2, RUNX1)** and **differentiation**.
- Increased variability in gene expression levels for differentiation-related markers in aged HSCs.

### 2. Chromatin Accessibility
- Aged HSCs displayed reduced accessibility in **promoter and enhancer regions** of stemness-related genes.
- Identification of **open DARs** enriched for **STAT, ATF, and CNC family transcription factor motifs**.

### 3. Integrated Analysis
- Strong correlation between chromatin accessibility and gene expression changes in aged HSCs.
- Open DARs in aged HSCs were linked to **enhanced transcriptional responses** under stress conditions.

---

## How to Reproduce the Analysis

### Prerequisites
- R (version 4.0 or higher)
- Seurat (for scRNA-seq analysis)
- ArchR (for ATAC-seq analysis)
- Additional R packages: `tidyverse`, `ggplot2`, `Signac`

### Steps
1. Download the data from [GEO (GSE190424)](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE190424).
2. Preprocess the data using the provided scripts in the `scripts/` directory.
3. Run the main analysis pipeline: `scripts/HSC_scRNA-ATAC_seq.Rmd`.
4. Visualize the results using the generated plots and tables in the `results/` directory.

---

## Citations
If you use this repository or the reproduced analysis in your work, please cite the original paper: Itokawa N, Oshima M, Koide S, Takayama N et al. Epigenetic traits inscribed in chromatin accessibility in aged hematopoietic stem cells. Nat Commun 2022 May 16;13(1):2691. PMID: 35577813.

---

## License
This project is licensed under the **MIT License**. 

