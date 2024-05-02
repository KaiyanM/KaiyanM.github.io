---
title: "[notes] Inferring Change Points in High-Dimensional Linear Regression via Approximate Message Passing"
date: 2024-04-01T15:34:30-04:00
categories:
  - Journal Reading
tags:
  - High-Dimensional
---

[original paper](https://ascopubs.org/doi/full/10.1200/JCO.22.01457)

For essays that shed light on the background and present research, it is relatively easy to make the structure apparent to the audience. However, it is not quite so for making it less brusque. Here are the opening paragraphs that I found as a case study to improve my writing.

> A new era of personalized medicine has arrived, which proposes an individualized health care model with tailored medical target treatment and management for each patient (Chin et al., 2011). Under this regime, not only clinical profiles of patients but also their molecular profiles are personally managed to drive for advanced treatment. Cancer studies that are focused on one-dimensional omics data have only provided limited information regarding the etiology of oncogenesis and tumor progression. To overcome this, tremendous efforts have been made to obtain multi-platform based genomic data from biospecimen.

Background introduction with specific cases to depict the application scenarios is way more reader-friendly than solely emphasizing the importance. (Question: how do you find or imagine the actual application? Especially when the topic came from a minor issue, though it's indeed helping for something, it's hard to make it both specific and not too niche.)

Multi-platform-based molecular profiles look like social networks and user portraits. Perhaps we can transfer some techniques between them.

> However, human genomes are complex and regulated at multiple levels, which can be manifested by various genomic assays mentioned above. While each of these assays offers a peek at the complex system, these events are rather interdependent (or interactive). Thus, when combining several different omics data to discover the coherent biological signatures, it is challenging to incorporate different biological layers of information to predict phenotypic outcomes (tumor/normal, early/late stage, survival, etc.). It is herein our goal to address the pressing and challenging issues for developing novel algorithms and theoretical methods for multi-omics data integration, in the hope to extract biologically meaningful information of clinical relevance.

Again, the structure is pretty straightforward: the problem, the present works are good but limited, our attempt, our challenge, and our goal. It's also helpful to use higher vocabulary to make it sound more professional, like **coherent biological signatures**, **incorporate**(instead of combine), **herein**(instead of thus), and **novel**(against new). 

localizing change points in high-dimensional linear regression
what is it
why it is important

Approximate Message Passing angorithm for estimatiing signals and change point location
usage: exploit prior informaion on signal noise and change points
benifit: enable uncertainty quantification with computable approximate posterior distribution

:D

## background intro
Heterogeneity in high-dimensional  datasets. 
> the hetero among features? days?
When the data are ordered by time, a simple form of heterogeneity is a change in the data generating mechanism at certain unknown instants of time. 

If these ‘change points’ were known, or estimated accurately, the dataset could be partitioned into homogeneous subsets, each amenable to analysis via standard statistical techniques (Fryzlewicz, 2014). 

Models with change points have been studied in a variety of statistical contexts, such as the detection of changes in: 
signal means (Wang & Samworth, 2018; Wang et al., 2020; Liu et al., 2021); 
covariance structures (Cho & Fryzlewicz, 2015; Wang et al., 2021b); 
graphs (Londschien et al., 2023; Bhattacharjee et al., 2020; Fan & Guan, 2018); 
dynamic networks (Wang et al., 2021a); and functionals (Madrid Padilla et al., 2022). 

Change pointmodels have found application in a range of fields including genomics (Braun et al., 2000), neuroscience (Aston & Kirch, 2012), and economics (Andreou & Ghysels, 2002).

## change points in high-dimensional linear regression

change points: sample indices where regression vector $\beta^{(i)}$ changes. number: $L*-1$
distinct signals: distinct signals in the sequence of $\beta^{(i)}$s. number: $L*$. upper bound: $L$

goal: estimate change point location and $L*$, also quantify uncertainty via confidence set or posterior distribution

recent works of high-dimentional linear regression with change points: 
Lee et al., 2016; Leonardi & Bu ̈hlmann, 2016; Kaul et al., 2019; Rinaldo et al., 2021; Xu et al., 2022; Li et al., 2023; Bai & Safikhani, 2023

Most of these papers consider the setting where the signals are sparse and analyze procedures that combine the LASSO estimator (or a variant) with a partitioning technique, e.g., dynamic programming. Although existing procedures for high-dimensional change point regression incorporate sparsity-based constraints, they cannot be easily adapted to take advantage of other kinds of signal priors. 
 > what kind of priors?
 Moreover, they are not well-equipped to exploit prior information on the change point locations. 
 > what prior information?
 
 Bayesian approaches to change point detection have been studied in several works, however they mainly focus on (low-dimensional) time-series.
 
 
 ##
 
 phi ? [L]^n ? [] is a set with sequence {1,2,....L}, so phi [L]^n is a vector where each element in the vector belong to that set separately
 
A[:,phi] see tissue



