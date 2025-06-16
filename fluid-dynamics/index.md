---
layout: default
title: "Foundational Model for Computational Physics"
permalink: /fluid-dynamics/
---



## Scalable Generative model for Computational Physics
Article title "SCALED : SCALable gEnerative founDational model for Computational Physics demonstrated on Urban Flow" under publication.

# Project Origin
This project stems from my dissertation in attempt to use **diffusion transformers** to model the computational fluid dynamics, inspired by OpenAI's **SORA** Video Generation (in 2024) to predict future frames. I developed the diffusion transformer from scratch which was able to replicate the PDE solver to a high degree of accuracy, trained on Imperial's HPC. However, the model lacked generalization capabilities as it was only usable on the trained scenario and resolution (ie not usable in other physics simulations), which is why our research group moved onto SCALED. 

# Project Overview
SCALED is a scalable foundational model built on a diffusion based generative framework for computational physics, developing a novel method to generalize computational fluid dynamics models to smaller or larger domains at any resolution. 

With inspiration from traditional numerical solvers, SCALED incorporates grid invariance and scale invariance by using through domain decomposition, with efficient boundary condition exchange across subdomains. SCALED massively outperforms state-of-the-art data-driven deep learning numerical solvers in multiple benchmarks.

We have demonstrated SCALED on a urban flow scenario with complex building geometries. Our tool has numerous applications in monitoring air quality and pollution in urban environments.

## My Responsibilities

- Helped conceptualize the generative model architecture
- 
- 🔬 Conducted hyperparameter tuning and model evaluation
- 📝 Authored significant portions of the research manuscript
- 🤝 Collaborated with domain experts in computational physics and AI

---

## Technologies Used

- PyTorch
- CUDA / GPU acceleration
- Jekyll / GitHub Pages (for this site)
- Scientific Python stack (NumPy, SciPy, Matplotlib)
- HPC cluster environments
