# 🌾 Wheat Breeding: Bayesian Modeling & Information Theory

[![Open Science](https://img.shields.io/badge/Open%20Science-ESALQ%2FUSP-success.svg)](#)
[![R](https://img.shields.io/badge/R-Pipeline-blue.svg)](#)

## 📖 About the Project
This repository contains the analytical pipeline developed for the "Mine" activity of the **Open Science** course at ESALQ/USP. The study evaluates the agronomic performance, adaptability, and stability of wheat cultivars (*Triticum aestivum* L.) cultivated under rainfed conditions in the Southern and Southeastern regions of Minas Gerais State, Brazil.

To overcome the limitations of rigid frequentist methods, this project introduces a fully data-driven pipeline that merges:
1. **Bayesian Hierarchical Mixed Models**: Utilizing the `rstanarm` package to natively absorb spatial constraints from the 4x4 Lattice layout and extract shrinkage-corrected posterior genetic estimates (Bayesian BLUPs).
2. **Information Theory Metrics**: Utilizing `infotheo` to map non-linear Genotype-by-Environment (GxE) networks via **Mutual Information**, quantify stability using **Shannon Entropy**, and dynamically assign weights for a Multi-Trait Selection Index based on informational channels.

## 📂 Repository Structure
* `Dados.xlsx`: Raw experimental phenotypic dataset (Yield, Hectoliter Weight, Thousand-Kernel Weight, Plant Height) collected across multiple environments.
* `Mutual Information for Plant Breeding.Rmd`: The core R Markdown script containing the fully reproducible pipeline.
* `Mutual-Information-for-Plant-Breeding.pdf`: The compiled scientific report containing narrative explanations, executable code, and high-resolution visualizations.
* `plots/`: Folder intended for the exported high-resolution PNG plots (e.g., GxE Reaction Norms, Environmental Heatmap, Selection Quadrants).

## ⚙️ How to Reproduce
To run this analysis locally and ensure strict reproducibility, follow these steps:

1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/wheat-bayesian-infotheory.git](https://github.com/your-username/wheat-bayesian-infotheory.git)
   ```

1. Open the R project or set your working directory to the cloned folder.

2. Ensure you have the following R packages installed:

```r
install.packages(c("tidyverse", "rstanarm", "tidybayes", "infotheo", "readxl"))

```
Note: rstanarm provides pre-compiled Stan models, meaning you do not need C++ compilers (like Rtools) configured on your machine to run the Bayesian sampling.

3. Open the Mutual Information for Plant Breeding.Rmd file and click Knit to compile the report and automatically generate the plot assets.
