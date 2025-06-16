---
layout: default
title: "Optimized C++ DNA alignment algorithm and mutation algorithm"
permalink: /c++-dna-alignment/
---

## Project Origin
Global Alignment (Needleman Wunsch) is a classic bioinformatics dynamic programming algorithm to compare pairs of entire DNA sequences for similarity. Similarily, Local Alignment (Smith-Waterman) compares core regions of sequences for similarity. 
<image>
 In our project at D24H, we needed to create mutated sequences 
 . For deep learning training, there are limited multithreaded C++/Python binded packages to be efficiently called thousands of times in batches. Hence, I have developed a package written in C++ and wrapped in PyBind optimized for deep learning, leveraging libtorch (Pytorch C++ API) for tensor implementation of the algorithm.


## DNA mutations
