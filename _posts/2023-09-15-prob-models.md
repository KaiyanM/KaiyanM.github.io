---
title: "Statistical Test"
date: 2023-09-15T15:34:30-04:00
categories:
  - Cheat Sheet
tags:
  - Statistical Test
---

## The Wilcoxon Rank Sum Test (Mann–Whitney U test)

 A non-parametric version of the two-sample t-test. **(non-parametric: does not assume the data have a known distribution described with math formulas.)** 
 
two-sample t-test assumptions:
> Independent
> Equal variance
> Normally distributed

Wilcoxon Rank Sum Test assumptions:
> Independent
> Equal variance

two-sample t-test H0:
> Equal means

Wilcoxon Rank Sum Test H0:
> Equal medians

The data in each group are first ordered from lowest to highest. Values in the entire data set, from both the control and treated groups, are then ranked, with the average rank being assigned to tied values as it is for the Wilcoxon rank-sum test. The ranks are then summed for each group, and U is determined as the smaller of:
$U_{1} = n_1n_2 + \frac{n_1(n_1+1)}{2}-R_1$
$U_{2} = n_1n_2 + \frac{n_2(n_2+1)}{2}-R_2$
