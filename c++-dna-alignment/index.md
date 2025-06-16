---
layout: default
title: "Optimized C++ DNA alignment algorithm and mutation algorithm"
permalink: /c++-dna-alignment/
---

## Project Origin
Global Alignment (Needleman Wunsch) is a classic bioinformatics dynamic programming algorithm to compare pairs of entire DNA sequences for similarity. Similarily, Local Alignment (Smith-Waterman) compares core regions of sequences for similarity. 
<image>

 In our project at D24H, we needed to create mutated sequences followed by an alignment of those mutated sequences with the original for deep learning. Therefore, we needed an efficient multithreaded package that can be called thousands of times in batches.
 There are limited multithreaded C++/Python binded packages of global alignment publicly available. Hence, I have developed a package written in C++ and wrapped in PyBind optimized for deep learning, leveraging libtorch (Pytorch C++ API) for tensor implementation of the algorithm.


## DNA mutations
