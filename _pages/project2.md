---
layout: archive
title: "Project2"
permalink: /project2/
author_profile: true
redirect_from:
  - /resume
kramdown:
  math_engine: mathjax
---

{% include base_path %}

# Surrogate-Assisted Distributional Modeling with Bias Correction

## Timeline: July 2025 - Present

## Research Focus
* **Imputation Methods**
* **Distributional Model**
* **Bias Correction**
* **Surrogate Assiated Statistical Inference**

## Overview

This research is motivated by challenges in electronic health records(EHR) analysis, where the true clinical outcome Y is difficult to obtain
because it is embedded in unstructured free-text notes. In contrast, surrogate variables S are easy to extract but are noisy, error-prone, 
and may include irrelevant or weakly informative proxies. Since these surrogates cannot be treated as the true outcome, out work develops a new method to reliably infer Y with the assiatnce of surrogate variables S based on a novel pre-additive noise distribution model called "Engression" from our previous work and explores the bias correction for such methods.
<div style="display:flex; justify-content:center; align-items:flex-start; gap:10px;">
  <img src="https://github.com/user-attachments/assets/caf2e422-66e9-4e16-8151-45c801d40685" width="445" height="254">
  <img width="529" height="235" alt="image" src="https://github.com/user-attachments/assets/2c27d48f-0e20-4eca-9d84-ea72af9c2a0b" />
</div>




## Previous Work
One important component of our proposed model is built upon the previous work of our team, which is a neural network-based distributional regression method called engression introduced in the paper "Engression: Extrapolation through the Lens of Distributional Regression?". This method provides a principled approach for modeling conditional distributions and has strong extrapolation properties. An open-source implementation and the paper of engression is available at: (https://github.com/xwshen51/engression)

In this paper, We propose a new method ‘engression’ for estimating the conditional distribution of a response variable given covariates and we showed that Engression in conjunction with pre-additive noise models provides a new perspective for the extrapolation problem in nonlinear regression.
<p align="center">
<img width="836" height="458" alt="image" src="https://github.com/user-attachments/assets/ee0fc35a-e46c-4b0f-bd12-2d7ae7436e64" />
</p>










