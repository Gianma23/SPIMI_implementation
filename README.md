# Information Retrieval system using an on-disk inverted index implementation

## Overview

This project implements an **Information Retrieval (IR)** system using an **on-disk inverted index**, built with the **SPIMI (Single-Pass In-Memory Indexing)** algorithm. It is designed to handle large-scale document collections that exceed memory limits, processing data in chunks and merging the intermediate indexes efficiently.

The system supports two retrieval models:
- **TF-IDF**
- **BM25**

Each model is tested using two access strategies:
- **Document-At-A-Time (DAAT)**
- **Term-At-A-Time (TAAT)**

Performance is evaluated using the **MS MARCO Passage Ranking** dataset and **TREC-DL 2020**, and results are compared to the established **PyTerrier** framework.

Moreover, the system implements a **LRU caching system** to store in memory the most recently used posting lists. This optimization drastically reduce the retrieving time from disk.

## Features

- On-disk index creation using SPIMI
- LRU Caching system for posting lists
- Modular design for testing IR models and strategies
- Performance benchmarking (ranking quality and efficiency)
- Comparison with PyTerrier baselines

## Getting started

The project is fully runnable on colab at the following link: https://colab.research.google.com/drive/1Ongut-DPE8qX9b0d5WwC0O0Qd4AvC3ln#scrollTo=9jdL5VVfoRnS

The inverted index is stored on a google drive folder and is downloaded automatically to avoid long computations. If you want to build from scratch the index, just remove the cell that downloads the files.