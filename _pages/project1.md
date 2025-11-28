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

## Working Papers & Preprint
   * Theory Part: Complex-time Representation, Kime-Phase Tomography, and Spacekime Analytics
      -   Anticipated to be on Arxiv at 12.25, 2025: [Link](/files/Kime_Algorithm.pdf)
   * Application Part: Learning Prediction and AI Modeling of Music Genre Perception Based on fMRI Data (Working) 
      -   Working Papers: [Link](aa.com)

## Timeline: Oct 2024 - Present

## Research Focus
 * **fMRI data analysis**
 * **Machine learning on spatiotemporal 3D data**
 * **Novel time series framework based on EM algorithm, Non-parametric pdf estimation, Weighted Least Squares, Fourier Series**  


## Overview

This is a multi-stage project consisting of 2 main parts: (1) a theoretical component developing the Spacekime Framework for time series analysis, and (2) an applied component implementing and evaluating the method on fMRI data analysis, in particular, focusing on understanding how discrete music categories are represented in human brain.

On the application side, our work is motivated by the 2021 study by Nakai T et al.,  **"Correspondence of categorical and feature-based representations of music in the human brain"** , which focused on classifying music through fMRI data. Given our long-standing interest in brain data analysis, we saw great space to extend this line of research and improve classification accuracy. This task also provides a suitable platform for evaluating our novel time-series modeling framework. Accordingly, we are currently preparing a manuscript that benchmarks state-of-the-art models for fMRI-based music classification and applies our proposed framework to this classification problem.
The following figure provides a visualization of the structure of the fMRI data we processed, to be precise, there are 10 different music genres to classify, fMRI signals were recorded every 1.5 seconds. During each run, each participant listened to 41 sgments of music, with each segment lasting 1.5, resulting in a total duration of 410 x 1.5 seconds.

The study by Nakai T et al. is available here: [Link](https://pubmed.ncbi.nlm.nih.gov/33164348/)

<p align="center">
  <img width="746" height="440" alt="image" src="https://github.com/user-attachments/assets/394c590b-125a-4c46-a056-68a9ed153a4d" />
</p>

On the theory side, we aim to propose a novel framework for fMRI time-series modeling based on the key assumptions that the observed fMRI signals are derived from a three-dimensional surface, where the x-axis representing time and the y-axis corresponds to an underlying latent angle variable. For this part, we are also preparing one paper intended to introduce the entire idea and showing some simulation results. 
Some key statistical knowledge we applied includes Weighted Least Squres, Fourier Transformation, Non-parametric pdf estimation. The following formula shows our key assumption of the structure of the data.

$$
Y_{j,k} = S(t_k, \theta_{j,k}) + \epsilon_{j,k}
= a_0(t_k) + \sum_{n=1}^{N_{harm}} \big[a_n(t_k)\cos(n\theta_{j,k}) + b_n(t_k)\sin(n\theta_{j,k})\big] + \epsilon_{j,k}
$$

$$
\begin{aligned}
& j = 1, 2, \dots, N \quad \text{(N individuals / repeated measurements)}\\
& k = 1, 2, \dots, K \quad \text{(K time steps)}\\
& \epsilon_{j,k} \sim N(0, \sigma^2)\\
& S(t, \theta) \text{ is represented using a finite-order Fourier expansion in } \theta
\end{aligned}
$$
<p align="center">
<img width="632" height="173" alt="image" src="https://github.com/user-attachments/assets/d430d529-0aaf-45ef-80bb-e9b4caa85ccd" />
</p>


##  General Idea in Glance
<iframe src="{{ site.baseurl }}/files/Kime_Algorithm.pdf" 
        width="100%" 
        height="600px" 
        style="border:1px solid #ccc;">
</iframe>

The correct display should look like this, please reach out to taozy@umich.edu if any error occurs: <br>
<p align="center">
<img width="500" height="403" alt="image" src="https://github.com/user-attachments/assets/b7a8945c-0a4a-43a9-9cc0-a86e94f0a0a0" />
</p>







