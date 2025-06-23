---
layout: default
title: "Deep Learning DNA Hash Database"
permalink: /dna-hash/
---

# Deep Learning DNA Hash
Similarity between DNA sequences is usually computed using [alignment](/cpp-dna-alignment), which is a dynamic programming problem of complexity **O(N2)**. 

Hence, searching through a DNA database is notoriously slow, as it cannot be computed using a simple euclidean distance. We develop a **novel** Transformer based similarity preserving DNA embeddings, and a subsequent database of the SRA Microbe (423,994 Files/ 2TB) is built and optimized for rapid searching. 

## Model Architecture
### Triplet Loss
Triplet Loss is a common technique used in training similarity-preserving embeddings (e.g. BERT), which uses an anchor (dog), a positive (labrador) and a negative (cat) to create embeddings. The distance between the embedding pairs are then computed and ensured to be at least a sufficient distance.

<Lebron image.>

### Model Architecture
Our model (Metagenomic Transformer) uses mutated sequences (in substitutions, insertions, deletions) to create the similar and dissimilar sequences, then uses a custom optimized alignment function to compute a **similarity score**. The lightweight transformer model (1.5M) then creates size 128 float embeddings and 128-bit binary hashes. The float embeddings stablize training and 128 bit hashes are for rapid searching and further compression. The loss is then computed to ensure the embedding distances are **exactly equal to the alignment scores**.
