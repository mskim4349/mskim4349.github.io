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
learning**. My research builds predictive material models that are *fast enough*
for design loops and *physical enough* to trust outside the training
distribution.

## Neural-Network Constitutive Modeling

**Motivation.** Classical elasto-plastic constitutive laws compress complex
path-dependent material behavior into a handful of phenomenological
parameters, trading expressive power for tractability. Plain neural-network
surrogates go the other way — they fit arbitrary stress responses but discard
the symmetries (frame indifference, the Clausius–Duhem inequality) that make a
constitutive law trustworthy outside its training distribution.

**Approach.** I parameterize the network input in **Haigh–Westergaard stress
invariants**, so the symmetry of the principal-stress space is exposed by
construction rather than learned from examples. A physics-consistent
data-augmentation scheme exploits material-frame indifference and
pressure–shear separability, generating synthetic training paths that respect
first-principles constraints.

**Findings.** The resulting model reproduces hardening behavior across loading
paths unseen during training, with substantially smaller data requirements than
naïve NN constitutive laws — the architecture itself carries the inductive
biases that data alone struggles to teach.

*Kim, Lee, Kim. Engineering Science and Technology, an International Journal
69, 102104 (2025).*

## Indentation-Based Inverse Identification

**Motivation.** Instrumented spherical indentation is one of the few mechanical
tests that scales to microscale specimens — thin films, single grains,
additively manufactured pillars. But classical Oliver–Pharr corrections
recover only a narrow set of properties, and they cannot separate residual
stress from intrinsic hardening when the surface is pre-stressed: both shift
the load–depth (P–h) curve in qualitatively similar ways.

**Approach.** I train artificial neural networks on parametric finite-element
sweeps of spherical-indentation P–h responses, learning the inverse map from a
single curve back to the underlying constitutive parameters — yield strength,
hardening exponent, hardening modulus. The framework extends naturally to
pre-stressed surfaces, where a single network simultaneously recovers material
properties and the residual-stress state from one curve.

**Findings.** Single-curve parameter identification covers hardening regimes
far outside the calibration window of analytical methods, and the
residual-stress extension disentangles two sources of P–h shift that
classical inverse methods conflate.

*Kim, Lee, Kim. Journal of Applied Mechanics 93(3), 031008 (2026).*
*Kim, Yoon, Chung. Journal of Applied Mechanics, submitted (2026).*

## Cryogenic-Environment Material Evaluation

**Motivation.** Marine liquid-hydrogen storage and fuel-supply systems operate
at 20 K, where austenitic stainless steels are the leading metallic-containment
candidate. Designing under IGF/IGC code-class safety requirements demands
more than tensile data: reliable fracture-toughness characterization at
cryogenic temperature is essential, and the J-resistance protocols
(unloading compliance vs. normalization method) give non-trivially different
answers in this regime.

**Approach.** Tensile and J–R fracture-toughness testing of 304L and 316L
stainless steels at cryogenic temperatures down to 20 K using a custom
cryostat, supplemented with electrochemical hydrogen-charging to bracket the
service environment. Computationally, I develop ductile-fracture models with
stress-state-dependent damage evolution that capture the multi-axial behavior
the tests probe, and contribute to four Korean Register (KRS) technical
reports on hydrogen-fuel marine applications.

**Findings.** Direct comparison of unloading-compliance and
normalization-method J–R analyses for 316L at 20 K, a ductile-fracture model
that holds across stress triaxialities for 304L, and a synthesized review of
the marine-LH₂ material-compatibility landscape.

*Kim, Lee, Kim. Theoretical and Applied Fracture Mechanics 132, 104474 (2024).*
*Kim, Cho, Jang. International Journal of Solids and Structures 318, 113439 (2025).*
*Kim, Chun. Journal of Marine Science and Engineering 11(10), 1927 (2023).*

## GNN Surrogates for Transient Multi-Physics

**Motivation.** Predicting welding residual stress and distortion at
production scale needs simulators that are accurate, generalize across
geometries and process parameters, and return *full fields* — not scalar
summaries. Conventional FE solves the full problem at prohibitive cost; plain
ANN surrogates predict only peak values or specific-point quantities; even
GNN simulators trained against dense FE labels inherit the labeling cost
that motivates surrogate modeling in the first place.

**Approach.** Label-free training of graph neural network surrogates via
**weak-form self-supervision**: the network is supervised by the residual
of the governing PDE in weak form, so dense ground-truth fields are never
required. Training-distribution coverage is enriched with **Gaussian random
field augmentation** of boundary and source conditions, including moving
heat sources representative of welding and laser-based thermal
manufacturing — the conditions that drive residual stress in the first
place.

**Findings.** *Work in progress.* The framework targets full-field
thermal–mechanical response under unseen heat-source trajectories, without
the dense FE-label budget that conventional GNN simulators require.

*Manuscript in preparation (2026).*
