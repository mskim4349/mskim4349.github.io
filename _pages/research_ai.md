---
layout: page
permalink: /research/ai/
title: AI for Accurate and Rapid Prediction
description:
nav: false
---

<style>
.rf-back{display:inline-block;margin-bottom:1rem;font-size:.95rem}
.rf-lead{font-size:1.05rem;margin:0 0 1.8rem}
.rf-sub{margin:1.6rem 0 2.4rem}
.rf-sub h2{font-size:1.25rem;margin:0 0 .5rem;border:0;padding:0}
.rf-sub ul{margin:0 0 .9rem;padding-left:1.15rem}
.rf-sub li{margin:.18rem 0;line-height:1.5}
.rf-fig2{text-align:center;margin:.6rem 0}
.rf-fig2 img{max-width:100%;width:820px;border-radius:8px;box-shadow:0 2px 12px rgba(0,0,0,.12);background:#fff;padding:6px}
</style>

<a class="rf-back" href="/research/">&larr; Research Field</a>

<p class="rf-lead">Machine-learning methods for material characterization, constitutive modelling, and fast surrogate simulation.</p>

<div class="rf-sub">
  <h2>Simultaneous Properties and Residual Stress</h2>
  <ul>
    <li>Neural networks recover constitutive parameters and the in-plane residual stress at the same time, from a single spherical-indentation curve and the residual imprint, separating effects that classical analysis cannot.</li>
  </ul>
  <div class="rf-fig2"><img src="/assets/img/research/detail/ai_residual_stress.png" alt="Simultaneous identification of properties and residual stress"></div>
</div>

<div class="rf-sub">
  <h2>Neural-Network Constitutive Modelling</h2>
  <ul>
    <li>A neural-network-integrated J2 elastoplastic model using Haigh-Westergaard inputs, more accurate and extrapolative than a principal-stress formulation.</li>
  </ul>
  <div class="rf-fig2"><img src="/assets/img/research/detail/ai_constitutive_nn.png" alt="Neural-network-integrated constitutive model"></div>
</div>

<div class="rf-sub">
  <h2>Graph-Neural-Network Surrogate for Transient Multi-Physics</h2>
  <ul>
    <li>Label-free surrogate for moving-heat-source problems, supervised by the weak form of the heat equation and trained by rollout.</li>
    <li>On a domain ten times larger than training, predicts about 11,000 time steps under 1 percent error, around 200 times faster than finite elements.</li>
  </ul>
  <div class="rf-fig2"><img src="/assets/img/research/detail/gnn_framework.svg" alt="Label-free graph-neural-network surrogate framework"></div>
  <div class="rf-fig2"><img src="/assets/img/research/detail/gnn_heat.svg" alt="Moving heat source on a domain ten times larger than training"></div>
</div>
