---
layout: page
title: Fine-Grained LLM Evaluations
description: DILL Lab research on capability structures for understanding reasoning failures in language models.
img:
importance: 1
category: ai-safety
---

I am working with USC's DILL Lab on fine-grained evaluations for reasoning in large language models. The project asks how to move beyond aggregate benchmark scores toward capability structures that make model weaknesses easier to diagnose.

My current work studies limitations of tree-shaped capability taxonomies such as EvalTree. Complex benchmark instances often exercise multiple capabilities at once, and those capabilities are not naturally forced into a single parent-child hierarchy. I have been exploring alternatives such as multi-capability annotations, axis-specific forests, and typed graph or graded-DAG representations that can express cross-cutting capabilities without duplicating the same concept in several branches.

The broader goal is to make evaluations sharper and more interpretable: define node accuracy by direct instance membership, compare structures against EvalTree's own weakness-identification metrics, and eventually use model-native information such as embeddings or sparse autoencoder features to reduce noisy LLM-generated labels.

This project connects most directly to my current AI safety interests: interpretability, evaluations, representation geometry, and designing probes that reveal how a model is reasoning rather than only whether it got the final answer right.
