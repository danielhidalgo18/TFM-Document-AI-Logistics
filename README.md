
# Comparative Evaluation of Document AI Architectures for Key Information Extraction in Industrial Logistics

This repository contains the source code and supplementary materials associated with the Bachelor's Thesis:

**"Comparative Evaluation of Document AI Architectures for Key Information Extraction in Industrial Logistics"**

## Abstract

Document processing remains a critical challenge in industrial logistics environments, where delivery notes, invoices, and transport documents are frequently received in heterogeneous formats and under varying acquisition conditions.

This project evaluates and compares three different Document AI paradigms:

- PaddleOCR + Regular Expressions (Rule-Based Pipeline)
- LayoutLMv3 (Multimodal Transformer)
- DONUT (Document Understanding Transformer)

The study focuses on the trade-off between:

- Information extraction accuracy
- Robustness against document degradation
- Computational efficiency

A synthetic dataset of Spanish logistics delivery notes was generated to perform controlled experiments under different levels of visual degradation.

---

## Repository Structure

```text
.
├── src/
│   ├── data_generation/
│   ├── augmentation/
│   ├── training/
│   ├── evaluation/
│   └── visualization/
│
├── examples/
│   ├── images/
│   └── annotations/
│
├── results/
│   ├── figures/
│   └── tables/
│
├── docs/
│   └── TFG_Daniel_Hidalgo.pdf
│
├── requirements.txt
├── LICENSE
└── README.md

