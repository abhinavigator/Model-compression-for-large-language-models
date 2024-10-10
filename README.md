# Model Compression on Large Language Models

## Introduction
This project explores model compression techniques for Large Language Models (LLMs), such as pruning, quantization, and knowledge distillation, to optimize them for resource-constrained environments. It focuses specifically on their application in text summarization and machine translation tasks, using CNN/Daily Mail and WMT 14 English-German datasets.

## Motivation
LLMs offer exceptional performance but come with high computational costs. Model compression techniques can reduce the size and complexity of these models, making them more suitable for deployment in real-world applications while balancing performance with efficiency.

## Problem Statement
The project aims to evaluate various model compression methodologies like pruning, quantization, and knowledge distillation within LLMs. The goal is to understand how these techniques impact tasks such as text summarization (using T5) and machine translation (using BART).

## Datasets
1. **CNN/Daily Mail Dataset**: Used for text summarization.
2. **WMT 14 English-German Dataset**: Used for translation tasks.

## Models
- **T5 (Text-to-Text Transfer Transformer)** for summarization.
- **BART (Bidirectional and Auto-Regressive Transformers)** for translation.

## Model Compression Techniques
The following compression techniques were explored:
- **Pruning**: Removes redundant parameters from the model.
- **Quantization**: Reduces precision of model parameters, such as weights.
- **Knowledge Distillation**: A smaller model (student) learns from a larger pre-trained model (teacher).

## Results
### Summarization Task (T5):
- Original T5: ROUGE-1: 45.02, ROUGE-L: 37.03
- Pruned T5: ROUGE-1: 39.3, ROUGE-L: 27.9
- Quantized T5: ROUGE-1: 39.2, ROUGE-L: 27.8
- Distilled T5: ROUGE-1: 36.7, ROUGE-L: 26.04

### Translation Task (BART):
- Original BART: BLEU: 37.5
- Pruned BART: BLEU: 26.3
- Quantized BART: BLEU: 28.4
- Distilled BART: BLEU: 36.3

## Conclusion
Model compression techniques like pruning, quantization, and distillation can effectively reduce the size of LLMs at the cost of some performance. Among the techniques, knowledge distillation offers the best trade-off between model size and task performance.

## References
1. [Chipman, Hugh A., et al. "BART: Bayesian additive regression trees." Annals of Applied Statistics, 2010.](https://projecteuclid.org/journals/annals-of-applied-statistics/volume-4/issue-1/Bayesian-additive-regression-trees/10.1214/09-AOAS285.short)
2. [Raffel, Colin, et al. "Exploring the limits of transfer learning with a unified text-to-text transformer." Journal of Machine Learning Research, 2020.](https://arxiv.org/abs/1910.10683)

