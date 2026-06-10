---
layout: page
title: Superposition and Steering Work Trial
description: MARS work-trial analysis of sparse feature encoding, interference, and activation geometry.
img:
importance: 5
category: ai-safety
---

For a MARS work trial with Francisco Ferreira da Silva, I analyzed a toy model where 100 sparse features are compressed through a 10-neuron bottleneck. The setup was meant to probe how models share representations, where interference appears, and how this relates to activation steering.

I evaluated per-feature mean squared error only when features were active, then studied isolated input-output responses for individual features. The learned functions were piecewise linear around the origin, and the slopes showed that the model was not learning independent ReLUs for each feature. Instead, it was using a shared approximate encoding.

I also swept the number of active features and found a near-linear increase in error, with the trained model losing its advantage over a naive baseline at high feature density. That pattern matched the superposition intuition: sparse regimes allow shared encodings to work, but dense regimes accumulate cross-term interference.

The part I found most interesting was the connection to steering. In the toy model, moving too many features through the bottleneck creates interference; in larger models, the analogous question is how to change activations enough to shift behavior without pushing them off-manifold and breaking coherence.
