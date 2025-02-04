# Text Summarization Evaluation and Ranking using TOPSIS

This repository provides a comprehensive framework for evaluating and ranking text summarization models using various metrics and the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method. The evaluation includes metrics like ROUGE, BLEU, readability, coverage, and redundancy, followed by the ranking of models based on their overall performance.

## Features

- **Text Summarization Metrics**: Includes evaluation of various summarization models using:
  - ROUGE-1, ROUGE-2, and ROUGE-L scores
  - BLEU score
  - Compression ratio
  - Readability score (Flesch Reading Ease)
  - Coverage (cosine similarity between original text and summary)
  - Redundancy (unique words ratio)

- **TOPSIS Ranking**: The models are ranked based on a weighted combination of the metrics using the **TOPSIS method**. The steps include:
  - **Normalization** of the performance metrics.
  - **Weight assignment** for each metric based on its importance.
  - Calculation of the **Ideal** and **Negative Ideal** solutions for each model.
  - **Euclidean distance** calculation for each model from the ideal and negative ideal solutions.
  - **TOPSIS score** calculation and ranking of the models based on the distance.

- **Models Evaluated**: The following text summarization models are evaluated using the TOPSIS method:
  1. **Extractive Summarization Model 1** (e.g., TF-IDF + Cosine Similarity)
  2. **Extractive Summarization Model 2** (e.g., LexRank)
  3. **Abstractive Summarization Model 1** (e.g., GPT-3)
  4. **Abstractive Summarization Model 2** (e.g., BART, T5)
  
- **Visualization**: Visualizations include:
  - Bar plots for TOPSIS scores by model
  - Heatmaps for metric comparison
  - Performance metrics comparison across models
  - Summary statistics for the best model

- **Output**: The final rankings and TOPSIS scores of the models are saved to a CSV file (`output.csv`), which can be further analyzed.

## Requirements

- Python 3.x
- Dependencies:
  - `nltk`
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `sklearn`
  - `rouge-score`
  - `textstat`


