---
title: "Exploring the halo-galaxy connection with probabilistic approaches"
collection: publications
permalink: 
excerpt: 'Normalizing flows, Gaussian Likelihood and regression to classification solving halo-galaxy scatter problem'
date: 2025-03-17
venue: 'A&A'
paperurl: 'https://www.aanda.org/articles/aa/full_html/2025/06/aa53284-24/aa53284-24.html'
citation: 'Rodrigues, N. V. N., de Santi, N. S. M., Abramo, R., et al. 2025, AAP, 698, A3. doi:10.1051/0004-6361/202453284'
---

**Abstract:**

The connection between galaxies and dark matter halos encompasses a range of processes and play a pivotal role in our understanding of galaxy formation and evolution. Traditionally, this link has been established through physical or empirical models. Machine learning techniques are adaptable tools that handle high-dimensional data and grasp associations between numerous attributes. In particular, probabilistic models capture the stochasticity inherent to these complex relations. We compare different probabilistic machine learning methods to model the uncertainty in the halo-galaxy connection and efficiently generate galaxy catalogs that faithfully resemble the reference sample by predicting joint distributions of central galaxy properties conditioned to their host halo features. The analysis is based on the IllustrisTNG300 simulation. The methods model the distributions in different ways. We compare a multilayer perceptron that predicts the parameters of a multivariate Gaussian distribution, a multilayer perceptron classifier, and the method of normalizing flows. The classifier predicts the parameters of a Categorical distribution, which are defined in a high-dimensional parameter space through a Voronoi cell-based hierarchical scheme. We evaluate the model's performances under various sample selections based on halo properties. The three methods exhibit comparable results, with normalizing flows showing the best performance in most scenarios. The models reproduce the main features of galaxy properties distributions with high-fidelity and reproduce the results obtained with traditional, deterministic, estimators. Our results also indicate that different halos and galaxy populations are subject to varying degrees of stochasticity, which has relevant implications for studies of large-scale structure.

You can read the paper [here](https://arxiv.org/abs/2301.06398).
