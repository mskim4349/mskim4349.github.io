---
layout: page
title: Multiscale GNN surrogate
description: Graph neural network surrogate for elasto-plastic FE² homogenization.
img: assets/img/12.jpg
importance: 1
category: research
related_publications: false
---

A graph neural network that replaces the microscale FE solve in an FE² simulation of
elasto-plastic composites. The microstructural mesh is encoded as a graph; node and edge
features carry the local strain history; the readout produces the homogenized stress and
the consistent tangent.

**What's interesting.** The architecture is **frame-indifferent by construction** (inputs
are rotated to the principal frame before message passing) and **history-aware** through a
GRU-style hidden state on the graph nodes. On benchmarks with random fiber-reinforced
microstructures, it achieves a ~500× speed-up over the reference FE² solve while keeping
the homogenized stress error below 2% across unseen loading paths.

**Status.** Manuscript under review at *CMAME*; code release planned with the camera-ready
version.
