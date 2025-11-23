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

## Timeline
I joined this project since July 2025.

## Overview

This research is motivated by challenges in electronic health records(EHR) analysis, where the true clinical outcome Y is difficult to obtain
because it is embedded in unstructured free-text notes. In contrast, surrogate variables S are easy to extract but are noisy, error-prone, 
and may include irrelevant or weakly informative proxies. Since these surrogates cannot be treated as the true outcome, out work develops a new method to reliably infer Y with the assiatnce of surrogate variables S based on a novel pre-additive noise distribution model called "Engression" from our previous work and explores the bias correction for such methods.

## Previous Work
One important component of our proposed model is built upon the previous work of our team, which is a neural network-based distributional regression method called engression introduced in the paper "Engression: Extrapolation through the Lens of Distributional Regression?". This method provides a principled approach for modeling conditional distributions and has strong extrapolation properties. An open-source implementation and the paper of engression is available at: https://github.com/xwshen51/engression




##  Latest Result
<iframe src="{{ site.baseurl }}/files/engression.pdf" 
        width="100%" 
        height="600px" 
        style="border:1px solid #ccc;">
</iframe>








