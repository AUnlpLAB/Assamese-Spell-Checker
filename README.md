# Assamese-Spell-Checker
This repository contains a comprehensive research framework for the detection of spelling errors in the Assamese language, a morphologically rich, low-resource Indo-Aryan language.

## Overview

The system follows a three-stage pipeline:
1. **Lexicon Generation:** Building a dictionary from Assamese Unicode text (`News.txt`).
2. **Error Detection:** Initial dictionary lookup.
3. **Error Correction:** Suggesting the Top-N corrections using Neural Embeddings and Similarity Metrics.

## Models Implemented

| Model ID | Architecture | Scoring / Clustering Metric |
| :--- | :--- | :--- |
| **Model 1** | CNN | Cosine Similarity |
| **Model 2** | CNN | Levenshtein Distance |
| **Model 3** | CNN | Jaro-Winkler |
| **Model 4** | **Hybrid** | CNN + Cosine + Levenshtein |
| **Model 5** | CNN | Agglomerative Clustering (Ward) |
| **Model 6** | CNN | K-Means Clustering |
| **Model 7** | GPT-2 | Semantic Cosine Similarity |
| **Model 8** | **IndicBERT** | Multilingual ALBERT Embeddings |
| **Model 9** | **MuRIL** | Google's Multilingual Representations |
| **Model 10**| **mBERT** | Baseline Multilingual BERT |

## Performance Metrics

Every model is benchmarked based on:
* **Accuracy:** Top-1 and Top-3 suggestion hits.
* **Latency:** Total execution time and seconds per word.
