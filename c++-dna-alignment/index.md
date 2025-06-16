---
layout: default
title: "Optimized C++ DNA Alignment and Mutation Algorithms"
permalink: /cpp-dna-alignment/
---

## Project Origin

Global alignment (Needleman-Wunsch) is a classical dynamic programming algorithm in bioinformatics, used to compare entire DNA sequences for similarity. Similarly, local alignment (Smith-Waterman) identifies and compares the most similar subsequences within a pair of DNA sequences.

![DNA Alignment Overview](your-image-link-here)

For our project at D24H, our deep learning workflow required two critical components:
1. **Generation of mutated DNA sequences**, and  
2. **Alignment of these mutated sequences with the original sequences**.

This process needed to be highly efficient, as alignment and mutation were performed thousands of times in batches during training.

While there are a few open-source C++/Python packages available, most do not support multithreading or are not optimized for deep learning workloads. Therefore, I developed a high-performance C++ package, wrapped with PyBind11 and integrated with libtorch (the C++ backend of PyTorch), enabling fast and parallelized alignment and mutation operations suitable for GPU workflows and batch tensor processing.

## Performance
Our package delivers speeds surpassing implementations from Biopython and Pyalign, including a multitude of options such as semi-global alignment, affine gap penalties, and mutation rates.
