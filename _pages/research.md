---
layout: page
permalink: /research/
title: research
description: 
nav: true
nav_order: 1
---

My research is about predicting how structural metals behave under demanding
service conditions, including very low temperatures, hydrogen exposure, and
large plastic deformation up to fracture. I work on this in three connected
ways: laboratory evaluation of mechanical and fracture properties, physics-based
finite-element models of damage and failure, and machine-learning methods that
either replace expensive simulations or recover properties that cannot be
measured directly. The four topics below describe the main lines of this work.

## Cryogenic and Hydrogen Materials Evaluation

{% include figure.liquid loading="eager" path="assets/img/research/cryo.png" class="img-fluid rounded z-depth-1" %}

- Tensile and fracture-toughness testing of austenitic stainless steels (304L, 316L) and aluminum alloys down to 20 K, the storage temperature of liquid hydrogen.
- Design and operation of a 20 K tensile and fracture-toughness cryostat with a helium re-liquefaction loop, one of the few such capabilities in Korea.
- A direct comparison of the unloading-compliance and normalization methods for J-resistance curves, with crack-length correction based on telecentric imaging of the crack front.
- Electrochemical and high-pressure gaseous hydrogen pre-charging to reproduce service exposure, relating the change in fracture mode to hydrogen.

*Related work: Theoretical and Applied Fracture Mechanics 132, 104474 (2024); Metals (2023); Processes 10(11), 2401 (2022).*

## Computational Damage Mechanics and Ductile Fracture

{% include figure.liquid path="assets/img/research/damage.png" class="img-fluid rounded z-depth-1" %}

- Stress-state-dependent ductile-damage models, written in terms of stress triaxiality and the third stress invariant, implemented as ABAQUS user-material subroutines (UMAT and VUMAT).
- Prediction of crack initiation and ductile failure of 304L stainless steel under multi-axial loading.
- Application to the impact failure of the primary barrier and insulation panel of a Mark-III LNG cargo containment system.

*Related work: International Journal of Solids and Structures 318, 113439 (2025); Metals (2022); Journal of Constructional Steel Research (2019).*

## Machine Learning for Inverse Material Characterization

{% include figure.liquid path="assets/img/research/ml.png" class="img-fluid rounded z-depth-1" %}

- Neural networks that recover constitutive parameters (elastic modulus, yield strength, and hardening parameters) from a single spherical-indentation load–depth curve together with the residual surface imprint.
- An extension that recovers the in-plane residual stress at the same time, separating two effects that classical indentation analysis cannot tell apart.
- A way to measure properties where standard specimens are not available, such as miniature samples or extreme-environment conditions.
- A related constitutive neural network based on Haigh–Westergaard stress invariants, which generalizes better with less training data by encoding material symmetry directly.

*Related work: Journal of Applied Mechanics 93(3), 031008 (2026); International Journal of Pressure Vessels and Piping, under review (2026); Engineering Science and Technology, an International Journal 69, 102104 (2025).*

## Graph-Neural-Network Surrogates for Transient Multi-Physics

{% include figure.liquid path="assets/img/research/gnn.png" class="img-fluid rounded z-depth-1" %}

- Graph-neural-network simulators trained without labelled data, supervised instead by the weak form of the governing equations, so that dense finite-element solutions are not needed for training.
- Gaussian-random-field augmentation of boundary and source conditions, including moving heat sources representative of welding and laser processing.
- Full-field thermal and mechanical predictions for unseen heat-source paths, at a small fraction of the cost of a conventional finite-element solve.

*Related work: manuscript in preparation (2026).*
