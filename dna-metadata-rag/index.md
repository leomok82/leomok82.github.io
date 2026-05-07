---
layout: default
title: "DNA Metadata Search RAG Database"
permalink: /dna-metadata-rag/
---

<section class="hero" style="padding-bottom: 40px;">
  <div class="hero-container" style="grid-template-columns: 1fr; text-align: center;">
    <div class="hero-content" style="max-width: 720px; margin: 0 auto;">
      <div class="section-label" style="justify-content: center;">Engineering Project</div>
      <h1>🧬 SRA Metadata <span class="highlight">RAG Search</span> Tool</h1>
      <p class="hero-subtitle">Natural language search over 35M+ genomic metadata records</p>
      <p class="hero-description">
        A powerful tool for natural language searching and filtering of Sequence Read Archive (SRA) metadata, enabling researchers to query large-scale genomic datasets from 583,982 studies with ease and precision.
      </p>
      <div class="tags" style="justify-content: center;">
        <span class="tag">LLMs</span>
        <span class="tag">BERT</span>
        <span class="tag">pgvector</span>
        <span class="tag">PostgreSQL</span>
        <span class="tag">Flask</span>
      </div>
    </div>
  </div>
</section>

<section class="section" style="padding-top: 0;">
  <div style="max-width: 860px; margin: 0 auto;">

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px; text-align: center;">
    <img src="/imgs/Home.jpeg" alt="SRA Metadata Search Tool" style="max-width: 90%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
  </div>

  <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px; margin-bottom: 24px;">
    <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 20px; color: var(--gray-900);">Algorithm Pipeline</h3>

    <div style="display: grid; gap: 16px;">
      <div style="padding: 16px; background: var(--gray-50); border-radius: var(--radius-sm);">
        <strong style="color: var(--blue-primary);">1. Query Formatting & Expansion</strong>
        <p style="color: var(--gray-600); font-size: 0.88rem; margin-top: 4px;">Gemini-2.0-flash-lite transforms natural language into structured categories — handles typos, translates languages, extracts metadata, and expands synonyms.</p>
      </div>
      <div style="padding: 16px; background: var(--gray-50); border-radius: var(--radius-sm);">
        <strong style="color: var(--blue-primary);">2. SQL Filtering</strong>
        <p style="color: var(--gray-600); font-size: 0.88rem; margin-top: 4px;">Combines semantic + user-defined filters into optimized PostgreSQL queries with indexed metadata fields.</p>
      </div>
      <div style="padding: 16px; background: var(--gray-50); border-radius: var(--radius-sm);">
        <strong style="color: var(--blue-primary);">3. Embedding Retrieval</strong>
        <p style="color: var(--gray-600); font-size: 0.88rem; margin-top: 4px;">SentenceTransformers (BERT-based) with Float16 embeddings and ANN retrieval via pgvector IVFFLAT index.</p>
      </div>
      <div style="padding: 16px; background: var(--gray-50); border-radius: var(--radius-sm);">
        <strong style="color: var(--blue-primary);">4. Reranking</strong>
        <p style="color: var(--gray-600); font-size: 0.88rem; margin-top: 4px;">JinaAI cross-encoder re-ranks results for context-aware ranking. Query speed: &lt;0.2s on 35M+ entries.</p>
      </div>
    </div>
  </div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 24px; margin-bottom: 24px;">
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 24px; text-align: center;">
      <h4 style="font-size: 0.95rem; font-weight: 600; margin-bottom: 12px; color: var(--gray-900);">Search by Study</h4>
      <img src="/imgs/SRA Metadata Study Result.jpeg" alt="Study search" style="width: 100%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
    </div>
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 24px; text-align: center;">
      <h4 style="font-size: 0.95rem; font-weight: 600; margin-bottom: 12px; color: var(--gray-900);">Search by Sample</h4>
      <img src="/imgs/example.png" alt="Sample search" style="width: 100%; border-radius: var(--radius-sm); border: 1px solid var(--gray-100);">
    </div>
  </div>

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 24px; margin-bottom: 24px;">
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">My Contributions</h3>
      <ul style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.8; list-style: none; padding: 0;">
        <li>• Backend & LLM integration</li>
        <li>• PostgreSQL and pgvector setup</li>
        <li>• Algorithm development</li>
      </ul>
    </div>
    <div style="background: var(--white); border-radius: var(--radius-lg); border: 1px solid var(--gray-100); padding: 32px;">
      <h3 style="font-size: 1.1rem; font-weight: 700; margin-bottom: 16px; color: var(--gray-900);">Stats</h3>
      <ul style="color: var(--gray-600); font-size: 0.92rem; line-height: 1.8; list-style: none; padding: 0;">
        <li>• <strong>35M+</strong> searchable entries</li>
        <li>• <strong>583,982</strong> studies indexed</li>
        <li>• <strong>&lt;0.2s</strong> query speed</li>
        <li>• <strong>$0.000243</strong> per query</li>
      </ul>
    </div>
  </div>

  <div style="background: var(--blue-light); border-radius: var(--radius-lg); padding: 24px 32px; margin-bottom: 24px;">
    <p style="color: var(--gray-700); font-size: 0.9rem; line-height: 1.6;">
      <strong>Team:</strong> Tracy Wong (Data curation, Frontend, PostgreSQL, Flask) & Leo Mok (Backend, LLM integration, pgvector, Algorithm). Built at D24H (HKU).
    </p>
  </div>

  <a href="/" class="contact-btn contact-btn-primary" style="display: inline-flex;">← Back to Home</a>

  </div>
</section>
