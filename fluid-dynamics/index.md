---
layout: default
title: "Foundational Model for Computational Physics"
---

<section class="hero" style="padding-bottom: 40px;">
  <div class="hero-container" style="grid-template-columns: 1fr; text-align: center;">
    <div class="hero-content" style="max-width: 720px; margin: 0 auto;">
      <div class="section-label" style="justify-content: center;">Research Project</div>
      <h1>Scalable Generative Model for <span class="highlight">Computational Physics</span></h1>
      <p class="hero-subtitle">SCALED: Demonstrated on Urban Flow Simulation</p>
      <p class="hero-description">
        A scalable foundational model built on a diffusion-based generative framework for CFD, achieving <strong>15x speedup</strong> over traditional solvers with domain decomposition and grid invariance.
      </p>
      <div class="tags" style="justify-content: center;">
        <span class="tag">PyTorch</span>
        <span class="tag">HPC / A100</span>
        <span class="tag">Diffusion Models</span>
        <span class="tag">Physics-Informed NN</span>
      </div>
    </div>
  </div>
</section>

<section class="section" style="padding-top: 0;">
  <div style="max-width: 860px; margin: 0 auto;">

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px;">
    <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">South Kensington Area Simulation</h3>
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
      <div style="text-align: center;">
        <img src="/imgs/pde_x.gif" alt="PDE Solver" style="width: 100%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
        <p style="font-size: 0.85rem; color: var(--gray-500); margin-top: 8px; font-weight: 500;">PDE Solver (Traditional)</p>
      </div>
      <div style="text-align: center;">
        <img src="/imgs/ai_x.gif" alt="SCALED" style="width: 100%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
        <p style="font-size: 0.85rem; color: var(--gray-500); margin-top: 8px; font-weight: 500;">SCALED (Neural Network)</p>
      </div>
    </div>
  </div>

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px;">
    <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Generated Unseen Area Simulation</h3>
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
      <div style="text-align: center;">
        <img src="/imgs/pde_x_gen.gif" alt="PDE Solver Generated" style="width: 100%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
        <p style="font-size: 0.85rem; color: var(--gray-500); margin-top: 8px; font-weight: 500;">PDE Solver (Traditional)</p>
      </div>
      <div style="text-align: center;">
        <img src="/imgs/ai_x_gen.gif" alt="SCALED Generated" style="width: 100%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
        <p style="font-size: 0.85rem; color: var(--gray-500); margin-top: 8px; font-weight: 500;">SCALED (Neural Network)</p>
      </div>
    </div>
  </div>

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px;">
    <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Benchmark Results</h3>
    <p style="color: var(--gray-600); margin-bottom: 16px;">SCALED outperforms state-of-the-art data-driven deep learning numerical solvers across multiple benchmarks.</p>
    <img src="/imgs/cfd_table.png" alt="Benchmark Table" style="width: 100%; border-radius: var(--radius-sm);">
  </div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 24px; margin-bottom: 24px;">
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">My Contributions</h3>
      <ul style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.8; list-style: none; padding: 0;">
        <li>• Authored portions of the manuscript</li>
        <li>• Conceptualized the generative model architecture</li>
        <li>• Ran benchmarks on HPC (4× A100)</li>
        <li>• Researched metrics including LSiM</li>
        <li>• Project conceptualization discussions</li>
      </ul>
    </div>
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Project Origin</h3>
      <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7;">
        Stems from my MSc dissertation at Imperial, exploring diffusion transformers for CFD inspired by OpenAI's SORA. The initial model replicated PDE solvers with high accuracy but lacked generalization — leading to SCALED's novel domain decomposition approach.
      </p>
    </div>
  </div>

  <div style="background: var(--blue-light); border-radius: var(--radius-lg); padding: 24px 32px; margin-bottom: 24px;">
    <p style="color: var(--gray-700); font-size: 0.9rem; line-height: 1.6;">
      <strong>Acknowledgements:</strong> First author is Yueyan Li, supervised by Professor Christopher Pain at the Applied Computational Modeling Group. Supported by the Department of Earth Science and Engineering at Imperial College London.
    </p>
  </div>

  <a href="/" class="contact-btn contact-btn-primary" style="display: inline-flex;">← Back to Home</a>

  </div>
</section>
