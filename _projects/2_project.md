---
layout: page
title: PINN inverse identification
description: Physics-informed neural networks for material parameter identification from instrumented indentation.
img: assets/img/7.jpg
importance: 2
category: research
related_publications: false
---

A physics-informed neural network framework that recovers elasto-plastic material
parameters (yield stress, hardening modulus, Hollomon exponent) directly from a single
instrumented load–depth curve, **without** needing the empirical Oliver–Pharr correction.

The PINN learns the displacement field under the indenter while satisfying the equilibrium
equation in residual form; the unknown material parameters are treated as additional
trainable variables. This sidesteps the ill-conditioning that plagues classical inverse
FE approaches when only one observable (P–h curve) is available.

**Why it matters.** Indentation is one of the few mechanical tests that works on
microscale samples (thin films, single grains, additively manufactured pillars). Reliable
parameter identification from a single curve unlocks high-throughput characterization.
