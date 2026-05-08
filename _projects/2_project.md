---
layout: page
title: NN-integrated elasto-plastic constitutive model
description: A neural-network constitutive law parameterized in Haigh–Westergaard coordinates with physics-aware data augmentation.
img: assets/img/7.jpg
importance: 2
category: research
related_publications: false
---

A neural-network constitutive model for elasto-plasticity, parameterized in
**Haigh–Westergaard stress coordinates** so the symmetry of the principal-stress
space is exposed to the network rather than learned from data. A
physics-consistent data-augmentation scheme exploits material-frame indifference
and pressure-shear separability to reduce the data needed for stable, accurate
hardening prediction.

**Why it matters.** Plain feed-forward NN constitutive laws train on raw stress
tensors, so they have to *re*-learn invariance under rotation and basic
thermodynamic constraints from examples. Building those into the parameterization
shrinks the data budget and improves extrapolation to unseen stress paths.

**Reference.** *A Neural Network-Integrated Elastoplastic Constitutive Model
Using Haigh–Westergaard Coordinates and Data Augmentation*, **Engineering
Science and Technology, an International Journal**, 69, 102104, 2025 —
[DOI](https://doi.org/10.1016/j.jestch.2025.102104).
