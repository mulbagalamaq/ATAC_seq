# Project Structure

```
single_cell/
├── README.md                 # Main project documentation
├── .gitignore               # Git ignore rules
├── single_cell.Rproj        # RStudio project file
├── PROJECT_STRUCTURE.md     # This file - project organization
├── scripts/                 # Analysis scripts
│   ├── HSC_scRNA-ATAC_seq.Rmd
│   └── Multiomic Analysis ATAC_seq.Rmd
├── data/                    # Raw and processed data
│   ├── GSM5723631_Young_HSC_*.h5
│   ├── GSM5723632_Aged_HSC_*.h5
│   └── *.tsv.gz
├── plots/                   # Generated plots and visualizations
│   ├── umap.png
│   ├── feature plot.png
│   ├── expression levels_violin plot.png
│   └── coverage plot_peaks.png
├── output/                  # Analysis outputs and results
├── results/                 # Processed results and tables
├── reports/                 # Generated reports and documents
└── docs/                    # Documentation and project files
    └── LICENSE
```

## Directory Descriptions

- **scripts/**: Contains all R Markdown analysis scripts
- **data/**: Raw data files (not tracked in git due to size)
- **plots/**: Generated visualizations and plots
- **output/**: Intermediate analysis outputs
- **results/**: Final processed results and tables
- **reports/**: Generated reports and documents
- **docs/**: Project documentation and legal files 