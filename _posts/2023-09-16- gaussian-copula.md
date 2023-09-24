---
title: " Gaussian Copula"
date: 2023-09-16T15:34:30-04:00
categories:
  - Cheat Sheet
tags:
  - Probability
---

## Wiki

The Gaussian copula is a distribution over the unit [[hypercube]] <math>[0,1]^d</math>. It is constructed from a [[multivariate normal distribution]] over <math>\mathbb{R}^d</math> by using the [[probability integral transform]].

For a given [[correlation matrix]] <math>R\in[-1, 1]^{d\times d}</math>, the Gaussian copula with parameter matrix <math>R</math> can be written as
:<math> C_R^{\text{Gauss}}(u) = \Phi_R\left(\Phi^{-1}(u_1),\dots, \Phi^{-1}(u_d) \right), </math>
where <math>\Phi^{-1}</math> is the inverse cumulative distribution function of a [[Standard normal#Standard normal distribution|standard normal]] and <math>\Phi_R</math> is the joint cumulative distribution function of a multivariate normal distribution with mean vector zero and covariance matrix equal to the correlation matrix <math>R</math>. While there is no simple analytical formula for the copula function, <math>C_R^{\text{Gauss}}(u)</math>, it can be upper or lower bounded, and  approximated using numerical integration.<ref name="bo16">{{cite journal|last1=Botev|first1=Z. I.|title=The normal law under linear restrictions: simulation and estimation via minimax tilting|journal=Journal of the Royal Statistical Society, Series B|volume=79|pages=125–148|date=2016|doi=10.1111/rssb.12162|arxiv=1603.04166|bibcode=2016arXiv160304166B|s2cid=88515228}}</ref><ref>{{cite web|url=https://cran.r-project.org/package=TruncatedNormal|title=TruncatedNormal: Truncated Multivariate Normal|first=Zdravko I.|last=Botev|date=10 November 2015|via=R-Packages}}</ref> The density can be written as<ref>{{cite journal |first=Philipp |last=Arbenz |year=2013 |title=Bayesian Copulae Distributions, with Application to Operational Risk Management—Some Comments |journal=Methodology and Computing in Applied Probability |volume=15 |issue=1 |pages=105–108 |doi=10.1007/s11009-011-9224-0 |hdl=20.500.11850/64244 |s2cid=121861059 |hdl-access=free }}</ref>
:<math> c_R^{\text{Gauss}}(u)
= \frac{1}{\sqrt{\det{R}}}\exp\left(-\frac{1}{2}
\begin{pmatrix}\Phi^{-1}(u_1)\\ \vdots \\ \Phi^{-1}(u_d)\end{pmatrix}^T \cdot
\left(R^{-1}-I\right) \cdot
\begin{pmatrix}\Phi^{-1}(u_1)\\ \vdots \\ \Phi^{-1}(u_d)\end{pmatrix}
\right), </math>
where <math>\mathbf{I}</math> is the identity matrix.
