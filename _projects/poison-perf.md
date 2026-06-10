---
layout: page
title: PoisonPerf
description: Data poisoning attacks in performative prediction.
img:
importance: 2
category: ai-safety
github: https://github.com/tetsnaga/poison-perf
---

[PoisonPerf](https://github.com/tetsnaga/poison-perf) is my semester project for a Trustworthy Machine Learning course. It studies data poisoning attacks in performative learning settings, where the deployed model changes the distribution of the future data it trains on.

Most poisoning work assumes a static data distribution. This project asks what happens when the learner, environment, and adversary interact over repeated retraining rounds. We implemented and compared poisoning attacks under multiple threat models, including black-box, white-box, and oracle-style adversaries.

I am proud of the project because it forced the code to mirror the conceptual structure of the problem. The data-generating process, attack methods, and performative retraining algorithms are separated cleanly enough that new attacks and environments can be added without rewriting the whole experiment.

This project is one of my clearest bridges into AI safety: it combines empirical ML, adversarial robustness, distribution shift, and the question of how deployed systems reshape the data they later learn from.
