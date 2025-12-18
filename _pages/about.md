---
permalink: /
title: "About me and this page"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hello there 👋! 

My name is [**Natalí de Santi**](http://lattes.cnpq.br/3869697280207128). 
I am a physicist working on statistical, computational, and machine learning (ML) methods applied to Cosmology and Astrophysics.

I am currently a Postdoctoral Scholar at the Berkeley Center for Cosmological Physics ([BCCP](https://bccp.berkeley.edu)), University of California, Berkeley ([UC Berkeley](https://www.berkeley.edu)), and an affiliated researcher at the Lawrence Berkeley National Laboratory ([LBL](https://www.lbl.gov)).

My main scientific interests include:
- large-scale structure of the Universe,  
- dark matter and dark energy,  
- cosmological parameter inference,  
- N-body and hydrodynamical simulations,  
- the halo-galaxy connection,  
- BAO reconstruction and parameter estimation.

Beyond Physics itself, I am deeply curious about data science, machine learning, probabilistic modeling, and scientific programming.

I obtained my PhD from the [University of São Paulo (USP)](https://www5.usp.br), under the supervision of  [Dr. Luis Raul Weber Abramo](http://lattes.cnpq.br/4558796258762790) (USP) and  [Dr. Francisco Villaescusa-Navarro](https://franciscovillaescusa.github.io/) (Flatiron Institute).  
My doctoral thesis focuses on how machine learning methods can be used to extract cosmological information from simulated halo and galaxy catalogs, and it is available [here](https://www.teses.usp.br/teses/disponiveis/43/43134/tde-15072024-101341/publico/tesenatalisolermatubarodesanti.pdf).

## A little **about me**

Since childhood, I have been fascinated by science, especially Astronomy and Physics, as well as by computers.  
As you can see in the picture below, when I was only four years old, I had a peculiar talent for drawing ducks in Microsoft Paint 🦆

![](https://raw.githubusercontent.com/natalidesanti/natalidesanti.github.io/master/images/4years.png)

This curiosity led me to participate in [Astronomy Olympiads](http://www.oba.org.br/site/) from an early age.  
During high school, I took part in experimental research on superconductivity with  
[Dr. Antonio Carlos Hernandes](http://lattes.cnpq.br/2019448857205643) at  
[USP São Carlos](https://saocarlos.usp.br/welcome-to-usp-sao-carlos/), an experience that ultimately convinced me to pursue Physics rather than Astronomy.

I completed my undergraduate studies at the [Institute of Physics of São Carlos (IFSC)](https://www2.ifsc.usp.br/english/), University of São Paulo.  
I initially worked on experimental materials physics within the former [CCMC](https://cdmf.org.br/) group, before transitioning to a more theoretical and computational path.  
My second undergraduate research project focused on Particle Physics, under the supervision of  
[Dr. Attilio Cucchieri](http://lattes.cnpq.br/5661661960969099).

For my master's degree, I moved to the [Federal University of São Carlos (UFSCar)](https://www.ufscar.br), working with [Dr. Raphael Santarelli](http://lattes.cnpq.br/3591899759824320).  
During this period, I studied General Relativity and Quantum Field Theory in Curved Spacetime, including work on Hawking radiation and the mass evolution of Schwarzschild black holes.
My research included a [review of Hawking radiation](http://www.scielo.br/scielo.php?script=sci_arttext&pid=S1806-11172019000300421&tlng=pt) and discussions on the [temporal evolution of a Schwarzschild black hole's mass](https://link.springer.com/article/10.1007/s13538-019-00708-y), taking this effect into account.

During my PhD, now fully focused on Cosmology, I joined the [University of São Paulo](https://www5.usp.br) in São Paulo and later spent a year as a guest researcher and  [CCA Predoctoral Fellow](https://www.simonsfoundation.org/flatiron-institute-center-for-computational-astrophysics-pre-doctoral-program) at the Flatiron Institute (2022-2023), my first long research experience abroad.

## Research interests and ongoing work

Broadly speaking, my research lies at the intersection of **cosmology**, **simulations**, and **machine learning**, with a focus on building robust, physically interpretable, and uncertainty-aware inference methods.

### 1️⃣ Field-level simulation-based inference for cosmology

A major part of my work focuses on **likelihood-free, field-level inference** using galaxy and halo catalogs.

- We showed that **graph neural networks (GNNs)** combined with **moment neural networks (MNNs)** can extract cosmological information directly from galaxy phase-space data, probing smaller scales than ever before, while remaining robust to astrophysical uncertainties. More details can be found [here](https://arxiv.org/abs/2302.14101).

- We extended this framework to include **observational effects**, such as masking, velocity and radial distance uncertainties, and galaxy selection, demonstrating that these models retain strong performance on realistic data ([paper](https://arxiv.org/abs/2310.15234)).

- By combining GNNs with **symbolic regression**, we extracted **analytic equations** that explain how these networks infer cosmological parameters, revealing physically interpretable relations that are robust across simulations and galaxy formation models ([paper](https://arxiv.org/abs/2302.14591)).

- Within the CAMELS project, we demonstrated that training on diverse hydrodynamical simulations, particularly **Astrid**, is key to building ML models that generalize across astrophysics and subgrid physics ([paper](https://arxiv.org/abs/2304.02096)).

- More recently, we showed that **semi-analytic models (SAMs)** can be used to train GNN-based inference models that extrapolate remarkably well to full hydrodynamical simulations, offering a fast and efficient path to cosmology-ready mock catalogs ([paper](https://arxiv.org/abs/2512.10222)).

### 2️⃣ Improving cosmological covariance matrices with machine learning

I also work on reducing the computational cost of cosmological analyses by improving covariance matrices.

- Using **convolutional neural networks** (CNNs), we developed a denoising approach that allows accurate covariance matrices to be constructed from only tens to hundreds of simulations, instead of tens of thousands, while preserving parameter inference accuracy  ([paper](https://arxiv.org/abs/2205.10881)). This work also showed its own extrapolation power after being trained on matrices using data from [ExSHalos](https://arxiv.org/abs/1906.06630) to data from the [Quijote simulations](https://quijote-simulations.readthedocs.io/en/latest/)
   
### 3️⃣ Modeling the halo-galaxy connection with probabilistic ML

Another core research direction is understanding and modeling the **stochastic nature of the halo-galaxy connection**.

- We used multiple ML models (ERT, LGBM, kNN, and NN) and data augmentation techniques ([SMOGN](https://github.com/nickkunz/smogn)) to predict galaxy properties from halo features, improving the description of scatter in halo-galaxy relations ([paper](https://arxiv.org/abs/2201.06054)).

- By reformulating regression as a classification problem, we recovered **full probability distributions** of galaxy properties for the first time ([paper](https://arxiv.org/abs/2301.06398)).

- We later compared different **probabilistic ML methods**, including a multivariate Gaussian distribution, a multilayer perceptron classifier, and normalizing flows, to identify which approaches best capture uncertainty in galaxy populations ([paper](https://arxiv.org/abs/2410.17844)).

## This page

This blog is a space where I share my research and related topics, ranging from **how we simulate the Universe on a computer** to **modern machine learning techniques for cosmology**, with the goal of making these ideas accessible while remaining scientifically rigorous.
