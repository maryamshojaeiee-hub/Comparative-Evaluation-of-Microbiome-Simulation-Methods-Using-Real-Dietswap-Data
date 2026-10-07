# Comparative-Evaluation-of-Microbiome-Simulation-Methods-Using-Real-Dietswap-Data
How realistic are simulated microbiome data? This project evaluates [MIDASim](https://github.com/mengyu-he/MIDASim) and compares it with three alternative simulators (MIDASim non-parametric mode, [SparseDOSSA2](https://github.com/biobakery/SparseDOSSA2) and [SPsimSeq](https://github.com/CenterForStatistics-UGent/SPsimSeq)), using the Dietswap gut microbiome study as a template.

Assignment for the course "Microbiome Data Analysis", Master of Statistics and Data Science (Bioinformatics), Hasselt University.

[Read the full report →](https://github.com/maryamshojaeiee-hub/Comparative-Evaluation-of-Microbiome-Simulation-Methods-Using-Real-Dietswap-Data/blob/main/report.pdf) · [View the code →](code/01_differential_expression.Rmd)

About the Project

New statistical methods for microbiome data are usually tested on simulated data, so their conclusions depend on how realistic the simulator is. This is difficult because microbiome data are sparse, overdispersed, compositional and correlated.

The evaluation compared real and simulated data on four taxon-level properties (mean abundance, variance, coefficient of variation and fraction of zeros) in three steps: the accuracy of a single simulated dataset, the consistency across 100 simulations, and a comparison with the other simulators.

Main finding: MIDASim in parametric mode reproduced the mean–variance structure of the real data well but struggled to capture sparsity, while the non-parametric and semi-parametric simulators reproduced the pattern of zeros more accurately.

Reproducing the Analysis

The Dietswap data are included in the microbiome package. The simulated datasets were generated separately with each simulator and saved as .RData files, which are not included in this repository because of their size; the report explains the settings used.

```r
install.packages(c("tidyverse", "patchwork", "knitr", "kableExtra", "ggridges", "viridis"))
if (!requireNamespace("BiocManager", quietly = TRUE)) install.packages("BiocManager")
BiocManager::install(c("phyloseq", "microbiome"))
```

Tools

R, R Markdown, phyloseq, microbiome, MIDASim, SparseDOSSA2, SPsimSeq, ggplot2

## Author
Maryam Shojaei Shahrokhabadi · [LinkedIn](https://www.linkedin.com/in/maryam-shojaei-210740250)· [maryam.shojaei.ee@gmail.com]
