---
layout: default
title: "CUDA C++ DNA Alignment and Mutation"
permalink: /cpp-dna-alignment/
---
# Optimized CUDA C++ DNA Alignment and Mutation Algorithms
## Project Origin

Global alignment (Needleman-Wunsch) is a classical dynamic programming algorithm in bioinformatics, used to compare entire DNA sequences for similarity. Similarly, local alignment (Smith-Waterman) identifies and compares the most similar subsequences within a pair of DNA sequences.

<img src="/imgs/images.png" alt="DNA Alignment Overview" width="600">

*Graphic from Journal of Computational Biology*

For our project at D24H, our deep learning workflow required two critical components:
1. **Generation of mutated DNA sequences**, and  
2. **Alignment of these mutated sequences with the original sequences**.

This process needed to be highly efficient, as alignment and mutation were performed thousands of times in batches during training.

While there are a few open-source C++/Python packages available, most do not support Python integration or are not optimized for deep learning workloads. Therefore, I developed a high-performance **CUDA** C++ package, wrapped with PyBind11 and integrated with libtorch (the C++ backend of PyTorch), enabling fast and parallelized alignment and mutation operations suitable for GPU workflows and batch tensor processing.

## CUDA
The CUDA version uses the Hirschberg Algorithm, a dynamic programming optimization which reduces space from 3 $O(N^2)$ matrices to two O(N) rows to compute the alignment score, which is crucial since GPU memory is limited. The implementation uses shared memory across blocks and performs one alignment per thread.

## Performance
Our package delivers speeds surpassing implementations from Biopython and Pyalign, including a multitude of options such as GPU, semi-global alignment, affine gap penalties, and mutation rates.

<a href="/" style="display: inline-block; padding: 10px 20px; background-color: #007acc; color: white; text-decoration: none; border-radius: 5px;">← Back to Home</a>
