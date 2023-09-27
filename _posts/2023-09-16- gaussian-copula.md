---
title: " Gaussian Copula"
date: 2023-09-16T15:34:30-04:00
categories:
  - Cheat Sheet
tags:
  - Probability
---

The name copula comes from the Latin for "link" or "tie", as it literally means this model is used to describe the inter-correlation between random variables. More specifically,  it is a multivariate CDF for which the marginal probability distribution of each variable is uniform on the interval [0, 1]. 

It's widely used in estimating high-dimensional applications since any multivariate joint distribution can be written in terms of univariate marginal distribution functions and a copula that describes the dependence structure between the variables, according to [Sklar's theorem](https://stats.stackexchange.com/questions/485219/derivation-of-sklars-theorem-for-copula#:~:text=Sklar's%20theorem%20states%20that%20the,copula%20of%20X%20and%20Y.)


1. Consider a random vector $$(X_{1},X_{2},\dots ,X_{d})$$, where marginal CDFs $${\displaystyle F_{i}(x)=\Pr[X_{i}\leq x]}$$  are continuous.
>Probability integral transform:
>Suppose that a random variable $$X$$ has a continuous distribution for which the CDF is $${\displaystyle F_{X}.}$$ Then the random variable $$U$$ defined as $${\displaystyle U:=F_{X}(X)\,,}$$ has a standard uniform distribution $$U[0,1]$$.

we can make a random vector $$(U_{1},U_{2},\dots ,U_{d})=\left(F_{1}(X_{1}),F_{2}(X_{2}),\dots ,F_{d}(X_{d})\right)$$, which has marginals be U[0,1]. The CDF of this random vector(aka The copula C) can be written as $${C=\displaystyle C(u_{1},u_{2},\dots ,u_{d})=\Pr[U_{1}\leq u_{1},U_{2}\leq u_{2},\dots ,U_{d}\leq u_{d}].}$$. 

### simulator 
The reverse of these steps can be used to generate pseudo-random samples from general classes of multivariate probability distributions. 
1. Generate a sample $$(U_{1},U_{2},\dots ,U_{d})$$ from the copula function.
2. Constructed $$(X_{1},X_{2},\dots ,X_{d})=\left(F_{1}^{-1}(U_{1}),F_{2}^{-1}(U_{2}),\dots ,F_{d}^{-1}(U_{d})\right)$$

Rewrite the above formula for the copula function with X:$${\displaystyle C(u_{1},u_{2},\dots ,u_{d})=\Pr[X_{1}\leq F_{1}^{-1}(u_{1}),X_{2}\leq F_{2}^{-1}(u_{2}),\dots ,X_{d}\leq F_{d}^{-1}(u_{d})].}$$

## Gaussian Copula

For a given correlation matrix $${\displaystyle R\in [-1,1]^{d\times d}}$$, the Gaussian copula with parameter matrix $$R$$ can be written as
$$C_{R}^{\text{Gauss}}(u)=\Phi _{R}\left(\Phi ^{-1}(u_{1}),\dots ,\Phi ^{-1}(u_{d})\right)$$

The Gaussian copula is a distribution over the unit =
${\displaystyle c_{R}^{\text{Gauss}}(u)={\frac {1}{\sqrt {\det {R}}}}\exp \left(-{\frac {1}{2}}{\begin{pmatrix}\Phi ^{-1}(u_{1})\\\vdots \\\Phi ^{-1}(u_{d})\end{pmatrix}}^{T}\cdot \left(R^{-1}-I\right)\cdot {\begin{pmatrix}\Phi ^{-1}(u_{1})\\\vdots \\\Phi ^{-1}(u_{d})\end{pmatrix}}\right),}$