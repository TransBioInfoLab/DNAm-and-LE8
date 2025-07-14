# **DNA Methylation Signatures of Life’s Essential 8 and Their Implications for Dementia**
David Lukacsovich, Liyong Wang, Wei Zhang, Lissette Gomez, Michael A. Schmidt, Hannah Gardener, Christian Agudelo, Juan I. Young, Eden R. Martin, Brian W. Kunkle, X. Steven Chen, Susan Blanton, Tatjana Rundek, Lily Wang

### Description

This github repository includes scripts used for the analyses in the above manuscript. 

**Background**

With rising dementia cases, there is a critical need for effective prevention strategies. Currently, objective biomarkers directly reflecting lifestyle modifications are limited. Life’s Essential 8 (LE8), comprising modifiable cardiovascular health factors, has been consistently linked to dementia risk.

**Objectives**

To identify DNA methylation biomarkers associated with LE8 scores and investigate their implications for dementia risk. 

**Design, Setting and Participants**

The Northern Manhattan Study (NOMAS) is a community-based urban cohort study. This analysis included DNA methylation samples from 273 stroke-free, self-identified Hispanic adults aged ≥ 40 years. 

**Measurements**

DNA methylation (DNAm) was assessed using Illumina MethylationEPIC arrays. Robust linear models and comb-p software identified CpGs and differentially methylated regions (DMRs) associated with LE8. Functional annotation, pathway analyses, and integrative analyses with gene expression, genetic variants, brain-blood correlations, and comparisons with independent dementia studies were conducted to nominate DNAm with converging evidence. 

**Results**

Adjusting for age, sex, APOE ε4, major immune cell proportions, genetic ancestry, and correcting genomic inflation, robust linear regression identified 11 CpGs at suggestive significance (P-value < 1×10-5). The comb-p software identified 37 significant DMRs associated with LE8 scores after multiple comparison correction. Pathway analyses showed LE8-associated DNAm were enriched in biological processes related to vascular integrity and inflammation, key pathways shared by cardiovascular disease and dementia. Integrative analyses showed several CpGs, notably in the HOXA5 gene promoter, that had significant blood-brain DNAm correlations, associations with gene expression and genetic variants, and were implicated in dementia neuropathology in previous independent studies. 

**Conclusions**

We found DNA methylation biomarkers derived from LE8 scores have significant roles in dementia, highlighting actionable targets for dementia prevention. Moreover, these biomarkers show strong clinical potential as objective measures to identify individuals at elevated risk, stratify participants based on biologically informed risk profiles, and monitor epigenetic responses to lifestyle interventions in secondary prevention trials aimed at reducing dementia risk. Future studies in larger and more diverse cohorts are needed to validate and refine these biomarkers for clinical applications. 

### Code Overview

**0. Collect Phenotype Information**

| File                                | Link                                                         |
| ----------------------------------- | ------------------------------------------------------------ |
| 00_get_phenotypes.Rmd               | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/00_get_phenotypes.Rmd) |

**1. Preprocess YR2021 Data**

| File                                | Link                                                         |
| ----------------------------------- | ------------------------------------------------------------ |
| 01a_get_data_EPIC112.Rmd            | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/01a_get_data_EPIC112.Rmd)            |
| 01b_filter_probes_EPIC112.Rmd       | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/01b_filter_probes_EPIC112.Rmd)       |
| 01c_impute_autosomal_EPIC112.Rmd    | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/01c_impute_autsomal_EPIC112.Rmd)     |
| 01d_normalize_autosomal_EPIC112.Rmd | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/01d_normalize_autosomal_EPIC112.Rmd) |
| 01e_pca_autosomal_EPIC112.Rmd       | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/01e_pca_autosomal_EPIC112.Rmd)       |

**2. Preprocess YR2019 Data**

| File                                | Link                                                         |
| ----------------------------------- | ------------------------------------------------------------ |
| 02a_get_data_EPIC208.Rmd            | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/02a_get_data_EPIC208.Rmd)            |
| 02b_filter_probes_EPIC208.Rmd       | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/02b_filter_probes_EPIC208.Rmd)       |
| 02c_impute_autosomal_EPIC208.Rmd    | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/02c_impute_autsomal_EPIC208.Rmd)     |
| 02d_normalize_autosomal_EPIC208.Rmd | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/02d_normalize_autosomal_EPIC208.Rmd) |
| 02e_pca_autosomal_EPIC208.Rmd       | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/02e_pca_autosomal_EPIC208.Rmd)       |

**3. Batch Correct Data**

| File                                | Link                                                         |
| ----------------------------------- | ------------------------------------------------------------ |
| 03a_batch_autosomal.Rmd             | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/03a_batch_autosomal.Rmd) |

**4. Linear Fit Against LE8 Score**

| File                           | Link                                                         |
| ------------------------------ | ------------------------------------------------------------ |
| 04a_prepare_training_data.Rmd  | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/04a_prepare_training_data.Rmd) |
| 04b_fit_robust_model.Rmd       | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/04b_fit_robust_model.Rmd)      |
| 04c_pathway_analysis.Rmd       | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/04c_pathway_analysis.Rmd)      |
| 04d_get_combp_inputs.Rmd       | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/04d_get_combp_inputs.Rmd)      |
| 04e_annotate_combp.Rmd         | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/04e_annotate_combp.Rmd)        |

**5. Compare to Prior Studies**

| File                            | Link                                                         |
| ------------------------------- | ------------------------------------------------------------ |
| 05a_get_signif_list.Rmd         | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/05a_get_signif_list.Rmd)         |
| 05b_brain_blood_correlation.Rmd | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/05b_brain_blood_correlation.Rmd) |
| 05c_eQTM_association.Rmd        | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/05c_eQTM_association.Rmd)        |
| 05d_manhattan_plot.Rmd          | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/05d_manhattan_plot.Rmd)          |
| 05e_reannot.Rmd                 | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/analysis/05e_reannot.Rmd)                 |

**Utility Functions**

| File                    | Link                                                         |
| ----------------------- | ------------------------------------------------------------ |
| detectionp_functions.R  | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/functions/detectionp_functions.R)  |
| run_parallel.R          | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/functions/run_parallel.R)          |
| run_pca.R               | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/functions/run_pca.R)               |

**External Functions**
The chronological age predictor code is replicated, as the code had to be modified to run as a function instead of a terminal command. The original code is found [here](https://github.com/qzhang314/DNAm-based-age-predictor).

| File                    | Link                                                         |
| ----------------------- | ------------------------------------------------------------ |
| pred_adjusted.R         | [Link to the script](https://github.com/TransBioInfoLab/DNAm-and-LE8/blob/main/code/DNAm-based-age-predictor-master/pred_adjusted.R)  |
