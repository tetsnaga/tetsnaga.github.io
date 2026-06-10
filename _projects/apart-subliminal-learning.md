---
layout: page
title: Subliminal Learning Experiments
description: Apart Research hackathon work on toy models of hidden bias transfer.
img:
importance: 3
category: ai-safety
---

For the AI Safety x Physics Grand Challenge hosted by Apart Research, I worked on experiments around subliminal learning: the phenomenon where a model can transmit a bias through training data that does not explicitly contain that bias.

Our team studied the simplest settings where this might occur. I contributed to the argument that linear regression cannot exhibit subliminal learning under the auxiliary-logit setup, replicated the MNIST classifier result in a small MLP, and helped extend the experiments to FashionMNIST and CIFAR-100.

I also investigated initialization sensitivity by adding noise to the student's initial weights and measuring when the subliminal-learning effect disappeared. The results supported the idea that shared initialization and representation alignment are central to the effect, which we also probed through cosine similarity between teacher and student hidden representations.

I have continued thinking about this work as a model organism for misalignment: small enough to study mechanistically, but close enough to real safety concerns around hidden generalization, poisoning, and representation-level transfer to be worth taking seriously.
