---
title: "Mimicking the halo-galaxy connection using machine learning"
collection: publications
permalink: 
excerpt: 'First approach: stacked methods and SMOGN'
date: 2022-01-16
venue: 'MNRAS'
paperurl: 'https://doi.org/10.1093/mnras/stac1469'
citation: 'Natalí S. M. de Santi, Natália V. N. Rodrigues, Antonio D. Montero-Dorta, L. Raul Abramo, Beatriz Tucci, M. Celeste Artale, Mimicking the halo–galaxy connection using machine learning, Monthly Notices of the Royal Astronomical Society, Volume 514, Issue 2, August 2022, Pages 2463–2478, https://doi.org/10.1093/mnras/stac1469'
---

**Abstract:**

Elucidating the connection between the properties of galaxies and the properties of their hosting haloes is a key element in theories of galaxy formation. When the spatial distribution of objects is also taken under consideration, investigating the halo-galaxy connection becomes very relevant for cosmological measurements. In this paper, we use machine learning (ML) techniques to analyze these intricate relations in the IllustrisTNG300 magnetohydrodynamical simulation. We employ four different algorithms: extremely randomized trees (ERT), K-nearest neighbors (kNN), light gradient boosting machine (LGBM), and neural networks (NN), along with a stacked model where we combine results from all four approaches. Overall, the different ML algorithms produce consistent results in terms of predicting galaxy properties from a set of input halo properties that include halo mass, concentration, spin, and halo overdensity. For stellar mass, the (predicted v. true) Pearson correlation coefficient is 0.98, dropping down to 0.7-0.8 for specific star formation rate (sSFR), colour, and size. In addition, we test an existing data augmentation technique, designed to alleviate the problem of unbalanced datasets, and show that it improves slightly the shape of the predicted distributions. We also demonstrate that our predictions are good enough to reproduce the power spectra of multiple galaxy populations, defined in terms of stellar mass, sSFR, colour, and size with high accuracy. Our results align with previous reports suggesting that certain galaxy properties cannot be reproduced using halo features alone.

You can read the paper [here](https://arxiv.org/abs/2201.06054).
