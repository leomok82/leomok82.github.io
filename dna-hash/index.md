---
layout: default
title: "Deep Learning DNA Hash Database"
permalink: /dna-hash/
---

<section class="hero" style="padding-bottom: 40px;">
  <div class="hero-container" style="grid-template-columns: 1fr; text-align: center;">
    <div class="hero-content" style="max-width: 720px; margin: 0 auto;">
      <div class="section-label" style="justify-content: center;">Research Project</div>
      <h1>Deep Learning <span class="highlight">DNA Hash</span> Database</h1>
      <p class="hero-subtitle">Transformer-based similarity-preserving embeddings for rapid DNA search</p>
      <p class="hero-description">
        DNA similarity is traditionally computed via alignment (O(N²)), making database search extremely slow. We develop <strong>novel Transformer-based similarity-preserving DNA embeddings</strong> with a searchable database of the SRA Microbe (423,994 files / 2TB).
      </p>
      <div class="tags" style="justify-content: center;">
        <span class="tag">PyTorch</span>
        <span class="tag">DDP / HPC</span>
        <span class="tag">Transformers</span>
        <span class="tag">SPARK</span>
      </div>
      <p style="font-size: 0.85rem; color: var(--gray-400); margin-top: 12px; font-style: italic;">Model architecture redacted — paper in progress</p>
    </div>
  </div>
</section>

<section class="section" style="padding-top: 0;">
  <div style="max-width: 860px; margin: 0 auto;">

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 24px; margin-bottom: 24px;">
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">My Contributions</h3>
      <ul style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.8; list-style: none; padding: 0;">
        <li>• Development of the PyTorch model (majority of codebase)</li>
        <li>• Training with DDP on HPC (V100, A40, H100)</li>
        <li>• Conceptualized transformer backbone & loss functions</li>
      </ul>
    </div>
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Triplet Loss</h3>
      <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7;">
        Common technique for training similarity-preserving embeddings (e.g. BERT). Uses anchor, positive, and negative examples to ensure embedding distances reflect true similarity.
      </p>
    </div>
  </div>

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px; text-align: center;">
    <img src="/imgs/triplet_loss.png" alt="Triplet Loss" style="max-width: 50%; border-radius: var(--radius-sm);">
    <p style="font-size: 0.8rem; color: var(--gray-400); margin-top: 8px;">Source: gombru.github.io</p>
  </div>

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px;">
    <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Model Overview</h3>
    <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7; margin-bottom: 16px;">
      Our Metagenomic Transformer uses mutated sequences (substitutions, insertions, deletions) to create similar/dissimilar pairs, with a custom optimized alignment function for similarity scores. The lightweight model (1.5M params) creates binary hashes with triplet loss ensuring embedding distance matches alignment score.
    </p>
    <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7;">
      Trained on SRA Reference Sequence (~200GB) using 4×H100 GPUs with distributed computing.
    </p>
  </div>

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px;">
    <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Database Construction</h3>
    <p style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.7; margin-bottom: 16px;">
      With the trained model, we compress sequences into a searchable database: sample representative regions via simple hashing → process batches with SPARK distributed computing → deduplicate into unique hash codes → apply traditional compression for rapid retrieval.
    </p>
    <img src="/imgs/MgDB.png" alt="Database Architecture" style="width: 100%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
  </div>

  <div style="background: var(--blue-light); border-radius: var(--radius-lg); padding: 24px 32px; margin-bottom: 24px;">
    <p style="color: var(--gray-700); font-size: 0.9rem; line-height: 1.6;">
      <strong>Acknowledgements:</strong> This project was done as a part of D24H (HKU). The research group leader and first author are in charge of publication and software distribution.
    </p>
  </div>

  <a href="/" class="contact-btn contact-btn-primary" style="display: inline-flex;">← Back to Home</a>

  </div>
</section>
