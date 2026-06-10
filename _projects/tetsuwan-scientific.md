---
layout: page
title: Tetsuwan Scientific
description: ML engineering for LLM- and vision-based laboratory automation systems.
img:
importance: 7
category: ml-research
---

At Tetsuwan Scientific, I worked as a Visiting Member of the Technical Staff on LLM- and computer-vision systems for lab automation.

I prototyped a multimodal agent that converted labware blueprints into structured JSON by combining OCR and LLMs while preserving spatial relationships between features. I also explored how to translate scientific intent into executable machine code, using LLMs for context-sensitive subtasks and rules-based models where determinism mattered more.

On the computer-vision side, I designed a standardized dataset for liquid-class calibration and trained a YOLO labware classifier. The most useful lesson was not just getting a model to train, but diagnosing what it had learned: in one case, overfitting to deck backgrounds and lighting rather than labware features, which I addressed with augmentation.

This work gave me a practical sense for the gap between impressive demos and reliable systems, a distinction that now matters a lot to how I think about AI safety and evaluations.
