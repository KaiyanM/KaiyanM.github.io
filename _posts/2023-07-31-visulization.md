---
title: "Muti-Omics Package Review"
date: 2023-07-31T16:34:30-04:00
categories:
  - research reading
Tags:
  - Muti-Omics
---

# Background

Multi-omics analysis inherits challenges from the single omics datasets and confounds further analyses with other new challenges of integration, clustering, functional characterization, and visualization.

There are 3 main challenges in dealing with multi-omics data,
1. Data Wrangling (includes various levels of “transformation” and “mapping”)
2. Data Heterogeneity (as these data are generated via varied technologies and platforms)
3. Dimension Reduction and Representation

# Packages

In the following parts, we are going to go over several popular packages for multi-omics and sum up their utility and drawbacks.

## MOVICS

Provides integrated analytic pipeline and creates many customizable visualizations for multi-omics integration and visualization in cancer subtyping. It incorporates the most commonly used downstream analyses in cancer subtyping research, including characterization and comparison of identified subtypes from multiple perspectives and verification of subtypes in external cohorts using two model-free approaches for multiclass prediction. 

### limitations: 
In sum, these visualizations are good at answering simple questions, like setting 20 clusters vs. 40 clusters, accepting the method or not; But are less helpful when facing Complex decisions, like what is the pattern in high-dimensional data.

## microViz

Provides a Shiny app for interactive exploration by pairing ordination plots and composition circular bar charts to show each taxon’s prevalence and abundance.

### limitations: 
Low interpretability of principal components.
Doesn’t contain much functionality designed for longitudinal data
Existing plots for longitudinal data are not ideal (provide too many bar plots, making it more difficult to extract the actual information asked for) 

## GWENA

gene co‑expression networks analysis and extended modules characterization in a single Bioconductor package to understand the underlying processes contributing to a disease or a phenotype.

### limitations: 
co-expression score based on correlation can only show the degree of common variation, which is less effective for predicting the variable of interest.
Only have feature network; The modules(groups) are computed between each pair of genes in the samples, thus are indirectly visualized.
The liner plot is overlapping and hard to read due to the large data size; can be simplified.

## NeVOmics

Facilitates the functional characterization of data from OMICs technologies.  It integrates Over-representation analysis(ORA) methodology and network-based visualization to show the enrichment results.

### limitations: 
Compatibility with: Windows and Linux; Depend on Python and R; Require some time to install and learn to use.
Not Dynamic, thus low transferability.
