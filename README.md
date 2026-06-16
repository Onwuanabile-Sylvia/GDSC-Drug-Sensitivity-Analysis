# Exploring Genomics of Drug Sensitivity in Cancer (GDSC): A Pharmacogenomic Analysis of Drug Response Across Cancer Cell Lines

---

## Author

### Sylvia Obiageli Onwuanabile

Medical Laboratory Scientist | Data Analyst | Aspiring Data Scientist

Interests:

* Healthcare Analytics
* Precision Medicine
* Bioinformatics
* Cancer Genomics
* AI-driven Healthcare Solutions

LinkedIn:

[www.linkedin.com/in/sylvia-onwuanabile](http://www.linkedin.com/in/sylvia-onwuanabile)

---


## Overview

Cancer drug response varies considerably across cancer types due to differences in their molecular, genetic, and biological characteristics. Understanding these differences is critical for precision oncology, where treatments are tailored to individual tumor profiles.

This project analyzes data from the **Genomics of Drug Sensitivity in Cancer (GDSC)** database to investigate patterns of drug sensitivity across cancer cell lines. Using exploratory data analysis, statistical testing, and biological pathway investigations, the study identifies sensitive and resistant cancers, effective and ineffective drugs, and molecular factors associated with treatment response.

The analysis demonstrates how pharmacogenomic data can be leveraged to uncover therapeutic vulnerabilities and support data-driven cancer research.

---

## Project Highlights

* Analyzed **162,103 drug–cancer observations** from the GDSC dataset.
* Evaluated drug sensitivity using **LN_IC50**, **AUC**, and **Z_SCORE** metrics.
* Identified the most effective and least effective anticancer compounds.
* Investigated cancer-type-specific drug responses across multiple tumor groups.
* Assessed the impact of genomic, transcriptomic, epigenomic, and biological factors on treatment response.
* Performed statistical testing and pathway-level analyses to uncover determinants of drug sensitivity.
* Generated publication-style visualizations to communicate key findings.

---

## Project Objectives

The primary objectives of this project were to:

* Explore the distribution of drug sensitivity metrics.
* Identify highly sensitive and resistant drugs.
* Compare drug response patterns across cancer types.
* Determine cancer-specific drug effectiveness.
* Investigate drug selectivity across cancers.
* Assess the influence of molecular features on treatment response.
* Examine the effects of microsatellite instability (MSI) and growth characteristics.
* Identify biological pathways associated with drug sensitivity.
* Generate clear visualizations that communicate key findings.

---

## Dataset

### Dataset Source

**Genomics of Drug Sensitivity in Cancer (GDSC)**

The GDSC project is one of the world's largest publicly available pharmacogenomic resources, containing drug response measurements across hundreds of anticancer compounds tested on cancer cell lines representing diverse tumor types.

Dataset obtained from:

HackBio Internship Public Datasets Repository

https://github.com/HackBio-Internship/public_datasets

### Key Variables

| Variable          | Description                       |
| ----------------- | --------------------------------- |
| DRUG_NAME         | Drug tested                       |
| TCGA_DESC         | Cancer type                       |
| LN_IC50           | Drug potency measurement          |
| AUC               | Overall drug response             |
| Z_SCORE           | Standardized sensitivity score    |
| TARGET_PATHWAY    | Drug target pathway               |
| CNA               | Copy Number Alteration indicator  |
| GEX               | Gene Expression indicator         |
| METHYLATION       | DNA methylation indicator         |
| MSI               | Microsatellite instability status |
| GROWTH_PROPERTIES | Cell growth characteristics       |

---

## Tools and Technologies

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy

### Development Environment

* Jupyter Notebook
* Anaconda
* GitHub

---

## Methodology

The analysis was conducted in several stages.

### 1. Data Preparation

* Loaded and explored the dataset.
* Examined variable types and dataset structure.
* Identified missing values.
* Performed data cleaning and validation.

### 2. Exploratory Data Analysis

* Examined distributions of LN_IC50, AUC, and Z_SCORE.
* Ranked drugs by sensitivity metrics.
* Identified resistant drug profiles.
* Investigated relationships among response variables.

### 3. Cancer-Type Analysis

* Compared drug responses across cancer types.
* Identified the most effective drug for each cancer type.
* Evaluated cancer-specific drug selectivity.

### 4. Molecular Analysis

Drug sensitivity was compared across:

* Copy Number Alteration (CNA) groups
* Gene Expression groups
* Methylation groups
* Microsatellite Instability (MSI) groups

### 5. Biological Analysis

* Investigated the impact of growth properties.
* Evaluated pathway-level drug sensitivity.
* Generated pathway heatmaps using Z_SCORE values.

### 6. Statistical Analysis

The Mann–Whitney U test was used to evaluate differences in drug sensitivity between MSI-H and MSS/MSI-L groups.

Correlation analyses were performed using Pearson correlation coefficients to assess relationships among LN_IC50, AUC, and Z_SCORE metrics.

---

## Key Findings

### Drug Sensitivity Patterns

The most potent drugs based on LN_IC50 included:

* Romidepsin
* Bortezomib
* Sepantronium bromide
* Docetaxel
* Daporinad

Romidepsin exhibited the lowest median LN_IC50 value, indicating exceptionally strong potency across cancer cell lines.

Using AUC as a complementary measure, the strongest inhibitors included:

* Sepantronium bromide
* Staurosporine
* CDK9_5038
* MG-132
* Dinaciclib

These compounds demonstrated broad activity across multiple cancer types.

### Drug Resistance Patterns

The least effective compounds included:

* Ascorbate (Vitamin C)
* N-acetyl cysteine
* Glutathione
* Alpha-lipoic acid
* Temozolomide

These drugs displayed relatively high LN_IC50 and AUC values, indicating weaker overall activity.

### Cancer-Specific Responses

Several cancer types demonstrated strong responses to specific drugs:

| Cancer Type | Most Sensitive Drug |
| ----------- | ------------------- |
| LCML        | Dasatinib           |
| MM          | Bortezomib          |
| ALL         | Daporinad           |

Drug response varied substantially across cancer types, highlighting the importance of personalized treatment strategies.

### Molecular Influences

Key observations included:

* CNA-positive cell lines showed slightly greater sensitivity.
* Gene expression status was associated with reduced sensitivity.
* Methylation demonstrated comparatively modest effects on drug response.

### Biological Influences

* MSI-H cell lines were significantly more sensitive than MSS/MSI-L cell lines.
* Suspension-growing cell lines generally exhibited greater sensitivity than adherent cell lines.

### Pathway Analysis

The most sensitive pathways included:

* Mitosis
* Cell Cycle
* DNA Replication
* Apoptosis Regulation
* Protein Stability and Degradation

These pathways represent important therapeutic vulnerabilities in cancer.

---

## Visualizations and Figures

The analysis generated several publication-style visualizations, including:

* Distribution plots of LN_IC50, AUC, and Z_SCORE.
* Drug sensitivity ranking plots.
* Drug resistance profiles.
* Cancer-type sensitivity heatmaps.
* Drug selectivity analyses.
* Molecular feature comparisons (CNA, Gene Expression, Methylation).
* Correlation matrices.
* MSI and growth property analyses.
* Target pathway sensitivity heatmaps.

---

## Repository Structure

```text
├── data/
│   └── GDSC.xlsx
│
├── notebooks/
│   └── Cancer_Drug_Sensitivity_Analysis_GDSC.ipynb
│
├── figures/
│   ├── Figure1_Global_Distributions.png
│
│   ├── Figure2A_SensitiveDrugs.png
│   ├── Figure2B_ResistantDrugs.png
│   ├── Figure2C_VariableDrugs.png
│
│   ├── Figure3_CancerType_Boxplot.png
│
│   ├── Figure4_DrugSensitivityHeatmap.png
│
│   ├── Figure5A_CNA_vs_LN_IC50.png
│   ├── Figure5B_CNA_vs_AUC.png
│   ├── Figure5C_GeneExpression_vs_LN_IC50
│   ├── Figure5D_GeneExpression_vs_AUC.png
│   ├── Figure5E_Methylation_vs_LN_IC50.png
│   ├── Figure5F_Methylation_vs_AUC.png
│
│   ├── Figure6A_LN_IC50_Histogram.png
│   ├── Figure6B_AUC_Histogram.png
│   ├── Figure6C_TopDrugs_Boxplot.png
│   ├── Figure6D_CancerTypes_Boxplot.png
│   ├── Figure6E_LN_IC50_vs_AUC_Scatter.png
│   ├── Figure6F_CorrelationHeatmap.png
│
│   └── Figure7_ZScore_Heatmap.png
│
├── README.md
│
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/Onwuanabile-Sylvia/GDSC-Drug-Sensitivity-Analysis.git
```

Navigate to the project folder:

```bash
cd Cancer_Drug_Sensitivity_Analysis_GDSC
```
Install required packages:

```bash
pip install -r requirements.txt
```

---

## Limitations

Several limitations should be considered:

* CNA, Gene Expression, and Methylation variables indicate data availability rather than quantitative measurements.
* Results are based on cancer cell lines and may not fully represent patient responses.
* Some cancer types contain relatively small sample sizes.
* Observed associations may be influenced by unmeasured biological factors.

---

## Future Work

Potential extensions of this analysis include:

* Incorporating mutation-level genomic information.
* Building predictive machine learning models for drug sensitivity.
* Integrating external pharmacogenomic datasets such as CCLE.
* Exploring biomarker discovery for personalized treatment selection.
* Developing interactive dashboards for drug response exploration.

---

## Conclusion

This analysis demonstrates that drug response is influenced by cancer type, molecular characteristics, growth properties, and biological pathways.

Hematological malignancies generally exhibited greater sensitivity than many solid tumors, while several drugs displayed strong cancer-type-specific activity. Molecular and pathway analyses further highlighted biological factors associated with treatment response.

Overall, the findings support the principles of precision oncology and demonstrate how pharmacogenomic data can be used to identify potential therapeutic vulnerabilities across cancers.

---

## References

1. Yang W, Soares J, Greninger P, et al. Genomics of Drug Sensitivity in Cancer (GDSC): A resource for therapeutic biomarker discovery in cancer cells. *Nucleic Acids Research*. 2013;41(Database issue):D955–D961.

2. Genomics of Drug Sensitivity in Cancer (GDSC). Wellcome Sanger Institute. https://www.cancerrxgene.org/

3. Iorio F, Knijnenburg TA, Vis DJ, et al. A landscape of pharmacogenomic interactions in cancer. *Cell*. 2016;166(3):740–754.

4. National Cancer Institute. TCGA Study Abbreviations. https://gdc.cancer.gov/resources-tcga-users/tcga-code-tables/tcga-study-abbreviations
