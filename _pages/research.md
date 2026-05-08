---
layout: about
title: research
permalink: /
subtitle: Postdoctoral Researcher · UNIST · Computational Solid Mechanics × Machine Learning

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false
  more_info: >
    <p>Department of Mechanical Engineering</p>
    <p>UNIST, 50 UNIST-gil, Eonyang-eup</p>
    <p>Ulju-gun, Ulsan 44919, South Korea</p>
    <p>📧 ms.kim [at] unist.ac.kr</p>

selected_papers: true
social: true

announcements:
  enabled: false
  scrollable: true
  limit: 5

latest_posts:
  enabled: false
  scrollable: true
  limit: 3
---

I work at the boundary between **computational solid mechanics** and **machine
learning**. The goal is to build predictive material models that are *fast
enough* for design loops and *physical enough* to trust outside the training
distribution.

#### Neural-network constitutive modeling
Constitutive laws for elasto-plasticity and ductile damage parameterized in
stress-invariant coordinates (Haigh–Westergaard) so the symmetry of the
principal-stress space is exposed to the network rather than learned from data.
Physics-consistent data augmentation reduces the training-data budget and
improves extrapolation across loading paths.

#### Indentation-based inverse identification
Recovering elasto-plastic parameters and residual stress from a single
spherical load–depth curve with artificial neural networks — a route to
high-throughput characterization of microscale specimens (thin films, single
grains, additively manufactured pillars) where classical Oliver–Pharr-style
corrections break down.

#### Cryogenic-environment material evaluation
Tensile and fracture-toughness characterization of austenitic stainless steels
(304L, 316L) at 20 K for liquid-hydrogen service, including unloading-compliance
and normalization-method J–R analyses, and ductile-fracture modeling under
multi-axial stress states.

#### GNN surrogates for transient multi-physics
Graph neural network simulators for moving heat-source problems (welding,
thermal manufacturing) trained without dense FE labels — weak-form
self-supervision with Gaussian random field augmentation — aiming to replace
expensive nonlinear FE solves while preserving full-field stress and
displacement information that scalar surrogates miss.
