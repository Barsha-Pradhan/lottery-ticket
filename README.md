# Model Compression using Intel Neural Compressor (OFA Pruning)

## Overview

This repository presents an experimental study on model compression using Intel Neural Compressor's One-Shot Optimization Framework (OFA) and BERT-base for Natural Language Processing tasks. The objective is to evaluate the impact of model optimization techniques on memory footprint, latency, throughput, energy consumption, and predictive performance across multiple GLUE benchmark datasets.

The experiments were conducted as part of a research internship project focusing on efficient deep learning and model compression.

---

## Method

The implementation follows the Intel Neural Compressor optimization workflow:

1. Load the pre-trained BERT-base model.
2. Apply optimization and compression techniques using Intel Neural Compressor (OFA framework).
3. Fine-tune and evaluate the model on GLUE benchmark datasets.
4. Measure:

   * Memory Size
   * Inference Latency
   * Accuracy
   * Precision
   * Recall
   * F1-score
   * Throughput
   * Energy Consumption

---

## Model

* Model: BERT-base-uncased
* Parameters: ~110 Million
* Precision: FP32 (32-bit)

---

## Datasets

The following GLUE benchmark datasets were evaluated:

* SST-2 (Sentiment Analysis)
* QNLI (Question Natural Language Inference)
* QQP (Quora Question Pairs)
* WNLI (Winograd Natural Language Inference)
* MNLI (Multi-Genre Natural Language Inference)
* MRPC (Microsoft Research Paraphrase Corpus)
* STS-B (Semantic Textual Similarity Benchmark)
* RTE (Recognizing Textual Entailment)
* CoLA (Corpus of Linguistic Acceptability)

---

## Experimental Results

| Dataset | Memory (MB) | Latency (ms) | Accuracy (%) | Precision (%) | Recall (%) | F1 (%) | Throughput (samples/s) | Energy (Wh) |
| ------- | ----------- | ------------ | ------------ | ------------- | ---------- | ------ | ---------------------- | ----------- |
| SST-2   | 417.65      | 2.90         | 92.20        | 92.21         | 92.20      | 92.20  | 344.93                 | 44.3366     |
| QNLI    | 417.65      | 2.2554       | 90.83        | 90.86         | 90.83      | 89.98  | 443.37                 | 17.733      |
| QQP     | 417.65      | 2.1501       | 83.79        | 81.79         | 81.88      | 82.17  | 465.10                 | 4.9911      |
| WNLI    | 417.65      | 4.8855       | 42.25        | 18.71         | 42.25      | 25.94  | 204.69                 | 0.7239      |
| MNLI    | 417.65      | 2.3058       | 68.73        | 69.48         | 68.73      | 68.75  | 433.68                 | 3.0184      |
| MRPC    | 417.65      | 5.16         | 84.80        | 85.11         | 94.27      | 89.46  | 193.90                 | 4.2240      |
| STS-B*  | 417.65      | 3.0576       | 89.88†       | N/A           | N/A        | N/A    | 327.06                 | 4.5953      |
| RTE     | 417.65      | 7.6886       | 70.40        | 71.68         | 61.83      | 66.39  | 130.06                 | 4.0616      |
| CoLA    | 417.65      | 1.6206       | 83.13        | 82.87         | 83.13      | 82.32  | 617.05                 | 4.4862      |

* STS-B is a regression task.
† Reported value corresponds to correlation-based performance.

---

## Environment

* Python 3.12
* Google Colab
* PyTorch
* Hugging Face Transformers
* Hugging Face Datasets
* Intel Neural Compressor
* NVIDIA Tesla T4 GPU

---

## Energy Consumption Estimation

Energy consumption was estimated using benchmark runtime and the typical power draw of an NVIDIA T4 GPU (~70 W). Since direct power measurements were not available in the Google Colab environment, the reported energy values are approximate and intended for comparative analysis only.

---



## References

1. Intel Neural Compressor
2. Hugging Face Transformers
3. GLUE Benchmark
4. BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding

---

## Author

Barsha Pradhan

Research Internship Project on Model Compression and Efficient Deep Learning
