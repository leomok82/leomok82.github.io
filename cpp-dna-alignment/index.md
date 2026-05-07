---
layout: default
title: "CUDA C++ DNA Alignment and Mutation"
permalink: /cpp-dna-alignment/
---

<section class="hero" style="padding-bottom: 40px;">
  <div class="hero-container" style="grid-template-columns: 1fr; text-align: center;">
    <div class="hero-content" style="max-width: 720px; margin: 0 auto;">
      <div class="section-label" style="justify-content: center;">Engineering Project</div>
      <h1>Optimized <span class="highlight">CUDA C++</span> DNA Alignment</h1>
      <p class="hero-subtitle">High-performance alignment & mutation algorithms for GPU workflows</p>
      <p class="hero-description">
        A high-performance CUDA C++ package for DNA alignment (Needleman-Wunsch, Smith-Waterman) and mutation, wrapped with PyBind11 and integrated with libtorch for batch tensor processing in deep learning pipelines.
      </p>
      <div class="tags" style="justify-content: center;">
        <span class="tag">CUDA</span>
        <span class="tag">C++</span>
        <span class="tag">PyBind11</span>
        <span class="tag">libtorch</span>
      </div>
    </div>
  </div>
</section>

<section class="section" style="padding-top: 0;">
  <div style="max-width: 860px; margin: 0 auto;">

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px; text-align: center;">
    <img src="/imgs/images.png" alt="DNA Alignment Overview" style="max-width: 80%; border-radius: var(--radius-sm);">
    <p style="font-size: 0.8rem; color: var(--gray-400); margin-top: 8px;">Graphic from Journal of Computational Biology</p>
  </div>

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px;">
    <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Motivation</h3>
    <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7;">
      Our deep learning workflow at D24H required efficient generation of mutated DNA sequences and alignment with originals — performed thousands of times per training batch. Existing open-source packages lack Python integration or optimization for DL workloads, so I developed this CUDA-accelerated package with PyBind11 wrapping.
    </p>
  </div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 24px; margin-bottom: 24px;">
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">CUDA Implementation</h3>
      <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7;">
        Uses the Hirschberg Algorithm — a DP optimization reducing space from 3× O(N²) matrices to two O(N) rows, crucial for limited GPU memory. Uses shared memory across blocks with one alignment per thread.
      </p>
    </div>
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Performance</h3>
      <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7;">
        Surpasses Biopython and Pyalign implementations. Supports GPU acceleration, semi-global alignment, affine gap penalties, and configurable mutation rates.
      </p>
    </div>
  </div>

  <a href="/" class="contact-btn contact-btn-primary" style="display: inline-flex;">← Back to Home</a>

  </div>
</section>
