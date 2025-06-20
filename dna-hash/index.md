---
layout: default
title: "Deep Learning DNA Hash Database"
permalink: /dna-hash/
---

# Deep Learning DNA Hash
Similarity between DNA sequences is usually computed using [alignment](/cpp-dna-alignment), which is a dynamic programming problem of complexity $$ O(N^2) $$. Hence, searching through a DNA database is notoriously slow, as it cannot be computed using a simple euclidean distance. We develop a **novel** Transformer based similarity preserving DNA embeddings, and a subsequent database of the SRA Microbe (423,994 Files/ 2TB) is built and optimized for rapid searching. 

