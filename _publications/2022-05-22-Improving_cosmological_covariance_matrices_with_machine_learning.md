---
title: "Improving cosmological covariance matrices with machine learning"
collection: publications
permalink: 
excerpt: 'Image denoising for a robust model'
date: 2022-09-06
venue: 'JCAP'
paperurl: 'https://iopscience.iop.org/article/10.1088/1475-7516/2022/09/013'
citation: 'de Santi, N. S. M. and Abramo, L. R. 2022, DOI:10.1088/1475-7516/2022/09/013'
---

**Abstract:**

Cosmological covariance matrices are fundamental for parameter inference, since they are responsible for propagating uncertainties from the data down to the model parameters. However, when data vectors are large, in order to estimate accurate and precise matrices we need huge numbers of observations, or rather costly simulations - neither of which may be viable. In this work we propose a machine learning approach to alleviate this problem in the context of the matrices used in the study of large-scale structure. With only a small amount of data (matrices built with samples of 50-200 halo power spectra) we are able to provide significantly improved matrices, which are almost indistinguishable from the ones built from much larger samples (thousands of spectra). In order to perform this task we trained convolutional neural networks to denoise the matrices, using in the training process a data set made up entirely of spectra extracted from simple, inexpensive halo simulations (mocks). We then show that the method not only removes the noise in the matrices of the cheap simulation, but it is also able to successfully denoise the matrices of halo power spectra from N-body simulations. We compare the denoised to the other matrices using several metrics, and in all of them they score better, without any signs of spurious artifacts. With the help of the Wishart distribution we derive an analytical extrapolation for the effective sample augmentation allowed by the denoiser. Finally, we show that, by using the denoised matrices, the cosmological parameters can be recovered with nearly the same accuracy as when using matrices built with a sample of 30,000 spectra in the case of the cheap simulations, and with 15,000 spectra in the case of the N-body simulations. Of particular interest is the bias in the Hubble parameter H0, which was significantly reduced after applying the denoiser.

You can read the paper [here](https://arxiv.org/pdf/2205.10881.pdf).
