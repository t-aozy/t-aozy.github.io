---
layout: archive
title: "Project1"
permalink: /project1/
author_profile: true
redirect_from:
  - /resume
kramdown:
  math_engine: mathjax
---

{% include base_path %}

# Spacekime Analytics:  <br> A Novel Framework for Time Series Modeling and fMRI Data Analysis

## Overview

This is a multi-stage project consisting of 2 main parts: (1) a theoretical component developing the Spacekime Framework for time series analysis, and (2) an applied component implementing and evaluating the method on fMRI data analysis, in particular, focusing on understanding how discrete music categories are represented in human brain.

In the application side, our interest was inspired by Nakai T's work **"Correspondence of categorical and feature-based representations of music in the human brain"** published in 2021, which focused on classifying music through fMRI data. Since Brain Data analysis is a long-term research interest of our team, we felt there were a lot more space left for us to explore in this topic, improving the classification accuracy. In addition, we consider this topic as a great experiment to test out our novel approach for Time Series Modeling. Thus for this part, we are drafting one paper and aims to find out the best existing models for classifying music from human brain, and to apply our novel framework on the classification task.

In the theory side, we propose a novel framework for fMRI time series modeling based on the key assumptions that the observed fMRI signals 
are derived from a three-dimensional surface, where the x-axis represents time and the y-axis corresponds to an underlying latent angle variable. For this part, we are also drafting one paper which is aiming to introduce the entire idea and showing some simulation results. 

$$
Y_{j,k} = S(t_k, \theta_{j,k}) + \epsilon_{j,k}
= a_0(t_k) + \sum_{n=1}^{N_{harm}} \big[a_n(t_k)\cos(n\theta_{j,k}) + b_n(t_k)\sin(n\theta_{j,k})\big] + \epsilon_{j,k}
$$

  - $j = 1, 2, \dots, N$ (N individuals / repeated measurements)  
  - $k = 1, 2, \dots, K$ (K time steps)  
  - $\epsilon_{j,k} \sim N(0, \sigma^2)$  
  - We represent $S(t, \theta)$ using a finite-order Fourier expansion in $\theta$.  
    The series is truncated at order $N_{harm}$, corresponding to $N_{harm}$ harmonic components.


## Working Papers

### Working Paper 1
Theory Part

### Working Paper 2
Application Part

##  General Idea in Glance
<iframe src="{{ site.baseurl }}/files/paper3.pdf" 
        width="100%" 
        height="600px" 
        style="border:1px solid #ccc;">
</iframe>







