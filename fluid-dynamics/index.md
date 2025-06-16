---
layout: default
title: "Foundational Model for Computational Physics"
permalink: /fluid-dynamics/
---



## Scalable Generative model for Computational Physics
Article title "SCALED : SCALable gEnerative founDational model for Computational Physics demonstrated on Urban Flow" under publication.

## Project Origin
This project stems from my Msc dissertation at Imperial, where I explored using **diffusion transformers** to model the computational fluid dynamics, inspired by *OpenAI's SORA Video Generation* (2024) to predict future frames. I developed the diffusion transformer capable of replicating the PDE solver to a high degree of accuracy, trained on Imperial's HPC. However, the model lacked generalization capabilities as it was restrictied to the trained scenario and resolution (ie not applicable to other physics simulations), which is why our research group moved onto SCALED. 

# Project Overview
SCALED is a scalable foundational model built on a **diffusion based generative framework** for computational physics, developing a novel method to generalize computational fluid dynamics models to smaller or larger domains at any resolution. With inspiration from traditional numerical solvers, SCALED incorporates grid invariance and scale invariance by using through domain decomposition, with efficient boundary condition exchange across subdomains. 

We have demonstrated SCALED on urban flow scenarios in the **South Kensington Area** as well as **generated unseen building geometries**, with a high degree of accuracy up to 750 time steps.  Our tool has numerous applications in monitoring air quality and pollution in urban environments.
{% raw %} 
<h3 style="text-align: center;">Computational Physics Simulation of the South Kensington Area</h3>

<div style="display: flex; justify-content: space-between; gap: 20px;">

  <div style="flex: 1; text-align: center;">
    <img src="/imgs/pde_x.gif" alt="Traditional Air flows" style="max-width: 100%;">
    <p><strong>PDE Solver (Traditional Approach)</strong></p>
  </div>

  <div style="flex: 1; text-align: center;">
    <img src="/imgs/ai_x.gif" alt="SCALED Air flows" style="max-width: 100%;">
    <p><strong>SCALED (Neural Network)</strong></p>
  </div>

</div>
<h3 style="text-align: center;">Computational Physics Simulation of the Generated Unseen Area</h3>

<div style="display: flex; justify-content: space-between; gap: 20px;">

  <div style="flex: 1; text-align: center;">
    <img src="/imgs/pde_x_gen.gif" alt="Traditional Air flows" style="max-width: 100%;">
    <p><strong>PDE Solver (Traditional Approach)</strong></p>
  </div>

  <div style="flex: 1; text-align: center;">
    <img src="/imgs/ai_x_gen.gif" alt="SCALED Air flows" style="max-width: 100%;">
    <p><strong>SCALED (Neural Network)</strong></p>
  </div>

</div>
{% endraw %} 
SCALED also outperforms state-of-the-art data-driven deep learning numerical solvers in multiple benchmarks.

![Benchmark Table](/imgs/cfd_table.png)

## My Responsibilities

- Authored portions of the manuscript
- Helped conceptualize the generative model architecture
- Ran benchmarks against other fluid dynamics neural networks on the HPC (4X A100)
- Researched additional metrics such as LSiM, which uses a neural network to compare similarity between volumes
- Involved with discussions for project conceptualization 

---

## Relevant Skills

- PyTorch
- HPC/Distributed Computing
- Physics informed Neural Networks
- Diffusion models

## Acknowledgements
The paper's first author is Yueyan Li and supervised by Professor Christopher Pain at the Applied Computational Modeling Group. The research is supported by the department of Earth Science and Engineering at Imperial College London. 

Please note that as this paper is still under submission, the manuscript is not yet sharable.
