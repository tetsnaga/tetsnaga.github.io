---
layout: page
title: Weight Decomposition for Interpretability
description: MARS work-trial experiments on decomposing learned weights into human-interpretable components.
img:
importance: 4
category: ai-safety
github: https://github.com/tetsnaga/bilinear-decomposition
---

For a MARS work trial connected to Thomas Dooms and Ward Gauderis's work on bilinear MLPs, I explored weight-based decompositions as a route to mechanistic interpretability.

The task centered on MNIST models and the problem that eigendecomposition often produces orthogonal components that are mathematically valid but not very human-interpretable. I experimented with priors that might recover cleaner reusable visual parts instead of digit-shaped or noisy superposed features.

The experiments pushed me to reason about interpretability as a design problem: sparsity helps, but it is not enough on its own; useful decompositions also need structure that reflects the geometry of the phenomenon. I tested ideas such as pixel sparsity, class-support priors, total variation smoothness, rank choices, and diversity penalties to move the components toward lines, curves, and shared digit parts.

The source task was based on the public [bilinear-decomposition](https://github.com/tetsnaga/bilinear-decomposition) repository.
