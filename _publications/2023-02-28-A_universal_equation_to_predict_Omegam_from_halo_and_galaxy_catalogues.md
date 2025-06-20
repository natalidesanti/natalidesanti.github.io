---
title: "A universal equation to predict Ωm from halo and galaxy catalogues"
collection: publications
permalink: 
excerpt: 'Using symbolic regression to understand GNNs'
date: 2023-02-28
venue: 'ApJ'
paperurl: 'https://iopscience.iop.org/article/10.3847/1538-4357/acee6f'
citation: 'Shao, H., de Santi, N. S. M., Villaescusa-Navarro, F., et al. 2023, ApJ, 956, 2, 149. doi:10.3847/1538-4357/acee6f'
---

**Abstract:**

We discover analytic equations that can infer the value of Ωm from the positions and velocity moduli of halo and galaxy catalogues. The equations are derived by combining a tailored graph neural network (GNN) architecture with symbolic regression. We first train the GNN on dark matter halos from Gadget N-body simulations to perform field-level likelihood-free inference, and show that our model can infer Ωm with ∼6% accuracy from halo catalogues of thousands of N-body simulations run with six different codes: Abacus, CUBEP3M, Gadget, Enzo, PKDGrav3, and Ramses. By applying symbolic regression to the different parts comprising the GNN, we derive equations that can predict Ωm from halo catalogues of simulations run with all of the above codes with accuracies similar to those of the GNN. We show that by tuning a single free parameter, our equations can also infer the value of Ωm from galaxy catalogues of thousands of state-of-the-art hydrodynamic simulations of the CAMELS project, each with a different astrophysics model, run with five distinct codes that employ different subgrid physics: IllustrisTNG, SIMBA, Astrid, Magneticum, SWIFT-EAGLE. Furthermore, the equations also perform well when tested on galaxy catalogues from simulations covering a vast region in parameter space that samples variations in 5 cosmological and 23 astrophysical parameters. We speculate that the equations may reflect the existence of a fundamental physics relation between the phase-space distribution of generic tracers and Ωm, one that is not affected by galaxy formation physics down to scales as small as 10 h−1kpc.

You can read the paper [here](https://arxiv.org/abs/2302.14591).
