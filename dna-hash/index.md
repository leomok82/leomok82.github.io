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
Triplet Loss is a common technique used in training similarity-preserving embeddings (e.g. BERT), which uses an anchor (dog), a positive (corgi) and a negative (cat) to create embeddings. The distance between the embedding pairs are then computed and ensured to be at least a sufficient distance. Below is an illustration of Triplet Loss 

<div>
  <img src="/imgs/triplet_loss.png" alt="SCALED Air flows" style="max-width: 50%; height: auto;">
</div>
(source: https://gombru.github.io/2019/04/03/ranking_loss/)


### Model Architecture
Our model (Metagenomic Transformer) uses mutated sequences (in substitutions, insertions, deletions) to create the similar and dissimilar sequences, then uses a custom optimized alignment function to compute a **similarity score**. The lightweight transformer model (1.5M) then creates size 128 float embeddings and 128-bit binary hashes. The loss is then computed to ensure the embedding distances are **exactly equal to the alignment scores**. 

The model was trained on SRA Reference Sequence (~200GB) using 4xH100 HPUs with GPU distributed computing.

<div>
  <img src="/imgs/hash_train.png" alt="SCALED Air flows" style="max-width: 100%; height: auto;">
</div>
### Database Construction
Then, with our trained model, we can now compress even more sequences into a searchable database. We first sample representative regions of each sequence (100-10000bp in length) using a simple hash function, reducing the data size. Then we use SPARK distributed computing to process batches of sequences which are then de-duplicated into a set of unique hash codes. Traditional database compression techniques are then leveraged to compress it into a smaller format but still effective at rapid retrieval.

<div>
  <img src="/imgs/MgDB.png" alt="SCALED Air flows" style="max-width: 100%; height: auto;">
</div>

### Project involvement
- Leading PyTorch code development, writing majority of the model's code base
- Optimized training process with **data-distributed parallel** (DDP) processing on the company's HPC (V100, A40, H100)
- Conceptualized significant parts of the model, such as the transformer backbone and loss functions.

### Acknowledgements
This project was done as a part of D24H (HKU). The research group leader and first author are in charge of the publication of the paper and distribution/commercialization of the software.
