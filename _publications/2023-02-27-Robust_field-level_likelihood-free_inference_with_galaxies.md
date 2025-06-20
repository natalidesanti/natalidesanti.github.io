---
title: "Robust field-level likelihood-free inference with galaxies"
collection: publications
permalink: 
excerpt: 'First ML robust method to predict $\Omega_{m}$'
date: 2023-02-27
venue: 'arXiv'
paperurl: 'https://iopscience.iop.org/article/10.3847/1538-4357/acd1e2/meta'
citation: 'Natalí S. M. de Santi et al 2023 ApJ 952 69'
---

**Abstract:**

We train graph neural networks to perform field-level likelihood-free inference using galaxy catalogs from state-of-the-art hydrodynamic simulations of the CAMELS project. Our models are rotationally, translationally, and permutation invariant and have no scale cutoff. By training on galaxy catalogs that only contain the 3D positions and radial velocities of approximately 1,000 galaxies in tiny volumes of (25 h−1Mpc)3, our models achieve a precision of approximately 12% when inferring the value of Ωm. To test the robustness of our models, we evaluated their performance on galaxy catalogs from thousands of hydrodynamic simulations, each with different efficiencies of supernova and AGN feedback, run with five different codes and subgrid models, including IllustrisTNG, SIMBA, Astrid, Magneticum, and SWIFT-EAGLE. Our results demonstrate that our models are robust to astrophysics, subgrid physics, and subhalo/galaxy finder changes. Furthermore, we test our models on 1,024 simulations that cover a vast region in parameter space - variations in 5 cosmological and 23 astrophysical parameters - finding that the model extrapolates really well. Including both positions and velocities are key to building robust models, and our results indicate that our networks have likely learned an underlying physical relation that does not depend on galaxy formation and is valid on scales larger than, at least, ∼10 h−1kpc.

You can read the paper [here](https://arxiv.org/abs/2302.14101).
