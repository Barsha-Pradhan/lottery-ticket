# 🎯 Lottery Ticket Hypothesis for NLP Model Compression

This repository explores the **Lottery Ticket Hypothesis (LTH)** for compressing transformer-based NLP models. The experiments were conducted using **BERT-base** on multiple **GLUE benchmark datasets** to evaluate model performance, efficiency, and resource utilization.

This work was completed as part of a **Research Internship** focused on **Model Compression, Neural Network Pruning, and Efficient Deep Learning**.

---

## 📌 Objectives

The primary objectives of this project are to:

- Investigate the Lottery Ticket Hypothesis for transformer models.
- Evaluate BERT-base across multiple GLUE benchmark datasets.
- Measure computational efficiency and predictive performance.
- Compare models using standard NLP evaluation metrics.

---

## 🧠 Model

- **Model:** BERT-base-uncased
- **Framework:** PyTorch
- **Library:** Hugging Face Transformers
- **Precision:** FP32 (32-bit)
- **Environment:** Google Colab
- **GPU:** NVIDIA Tesla T4

---

## 📚 Datasets

The experiments were conducted on the following GLUE benchmark datasets:

- SST-2 (Sentiment Analysis)
- QNLI (Question Natural Language Inference)
- QQP (Quora Question Pairs)
- WNLI (Winograd Natural Language Inference)
- MNLI (Multi-Genre Natural Language Inference)
- MRPC (Microsoft Research Paraphrase Corpus)
- STS-B (Semantic Textual Similarity Benchmark)
- RTE (Recognizing Textual Entailment)
- CoLA (Corpus of Linguistic Acceptability)

---

## 📊 Experimental Results

| Dataset | Memory (MB) | Latency (ms) | Accuracy (%) | Precision (%) | Recall (%) | F1-score (%) | Throughput (samples/sec) |
|----------|------------:|-------------:|-------------:|--------------:|-----------:|-------------:|-------------------------:|
| SST-2 | 417.65 | 2.90 | 92.20 | 92.21 | 92.20 | 92.20 | 344.93 |
| QNLI | 417.65 | 2.2554 | 90.83 | 90.86 | 90.83 | 89.98 | 443.37 |
| QQP | 417.65 | 2.1501 | 83.79 | 81.79 | 81.88 | 82.17 | 465.10 |
| WNLI | 417.65 | 4.8855 | 42.25 | 18.71 | 42.25 | 25.94 | 204.69 |
| MNLI | 417.65 | 2.3058 | 68.73 | 69.48 | 68.73 | 68.75 | 433.68 |
| MRPC | 417.65 | 5.16 | 84.80 | 85.11 | 94.27 | 89.46 | 193.90 |
| STS-B* | 417.65 | 3.0576 | Pearson: 0.8988 | N/A | N/A | N/A | 327.06 |
| RTE | 417.65 | 7.6886 | 70.40 | 71.68 | 61.83 | 66.39 | 130.06 |
| CoLA | 417.65 | 1.6206 | 83.13 | 82.87 | 83.13 | 82.32 | 617.05 |

> **Note:** STS-B is a regression task and is evaluated using **Pearson** and **Spearman** correlation instead of Accuracy, Precision, Recall, and F1-score.

---

## ⚡ Energy Consumption

Energy consumption was estimated using the benchmark runtime and the typical power draw of an NVIDIA Tesla T4 GPU (~70 W). Since direct power measurements were not available in the Google Colab environment, the reported energy values are approximate and intended for comparative analysis.

---

## 🛠 Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Scikit-learn
- NumPy
- Google Colab

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/Barsha-Pradhan/lottery-ticket.git
cd lottery-ticket
```

Install dependencies:

```bash
pip install transformers datasets evaluate accelerate scikit-learn numpy
```

---

## 📂 Repository Structure

```
lottery-ticket/
│
├── SST2/
├── QNLI/
├── QQP/
├── WNLI/
├── MNLI/
├── MRPC/
├── STSB/
├── RTE/
├── COLA/
├── README.md
└── requirements.txt
```

---

## 📖 References

- Frankle, J., & Carbin, M. (2019). *The Lottery Ticket Hypothesis: Finding Sparse, Trainable Neural Networks.*
- Devlin, J., Chang, M. W., Lee, K., & Toutanova, K. (2019). *BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding.*
- GLUE Benchmark
- Hugging Face Transformers

---

## 👩‍💻 Author

**Barsha Pradhan**

Research Internship Project on **Model Compression**, **Lottery Ticket Hypothesis**, and **Efficient NLP Models**.
