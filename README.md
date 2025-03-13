# Information-Retrieval-Project
Course: Information Retrieval - Università degli Studi di Milano Bicocca

## Introduction:
This project explores various retrieval techniques for the NFCorpus dataset, analyzing the effectiveness of different indexing, retrieval, and ranking strategies. The goal is to improve document retrieval performance through statistical models (TF-IDF, BM25), query expansion, and neural re-ranking.

## Methods:
- Dataset Analysis: Examined document and query length distributions, word frequency, and relevance judgments.
- Retrieval Models: Implemented TF-IDF and BM25, testing six indexing pipelines with different preprocessing strategies (stemming, stopword removal, title vs. full-text indexing).
- Query Expansion: Used Word2Vec to expand queries with semantically related terms, but results degraded due to noise.
- Neural Re-Ranking: Applied two transformer-based models:
  1) Tomaarsen/static-retrieval-mrl-en-v1
  2) All-MiniLM-L6-v2, which achieved the best results.

## Evaluation Metrics:
- MAP (Mean Average Precision)
- P@10 (Precision at top 10 results)
- nDCG@10 (Normalized Discounted Cumulative Gain)

## Results & Conclusions:
BM25 outperformed TF-IDF across all pipelines.
Query expansion did not improve retrieval, likely due to the introduction of irrelevant terms.
Neural re-ranking significantly enhanced performance, with All-MiniLM-L6-v2 achieving the best results in terms of MAP, P@10, and nDCG@10.
Future improvements: Fine-tuning reranking models on domain-specific data and exploring alternative query expansion methods.
This project highlights the importance of neural ranking models in improving traditional retrieval approaches and provides a foundation for further optimization in information retrieval tasks.
