---
layout: default
title: "Optimized C++ DNA alignment algorithm and mutation algorithm"
permalink: /c++-dna-alignment/
---

# DNA Alignment tool
Global Alignment (Needleman Wunsch) is a classic bioinformatics dynamic programming algorithm to compare pairs of entire DNA sequences for similarity. Similarily, Local Alignment (Smith-Waterman) compares core regions of sequences for similarity. 

For deep learning training, there are limited multithreaded C++/Python binded packages to efficiently integrate into training. Hence, I have developed a package written in C++ and wrapped in PyBind optimized for deep learning, leveraging libtorch (Pytorch C++ API) for tensor implementation of the algorithm.
