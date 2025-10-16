# AgriChatBot-Summative
🌾 Agribot T5 Models

This repository contains fine-tuned T5 language models developed for the Agribot Project — an AI assistant designed to understand and respond to agricultural queries. Each model represents a different experimental configuration, optimized for BLEU, F1-Score, and Perplexity metrics.

🧠 Overview

The models were fine-tuned using a text-to-text approach based on the T5 architecture, where both the input and output are represented as natural language. This enables the model to generalize across multiple NLP tasks such as summarization, Q&A, and agricultural advice generation.

The text preprocessing follows a minimalist normalization strategy to retain meaning while removing noise like URLs, HTML tags, and irregular spacing.

⚙️ Model Configurations

| Model ID             | Batch Size | Learning Rate | Dropout | Regularizer | Epochs | Optimizer | BLEU   | F1-Score | Perplexity |
| -------------------- | ---------- | ------------- | ------- | ----------- | ------ | --------- | ------ | -------- | ---------- |
| **FinalModel**       | 32         | 1e-4          | 0.15    | 1e-5        | 30     | Nadam     | 0.1016 | 0.2968   | 9.1979     |
| **Premium Improved** | 32         | 7e-4          | 0.15    | 1e-5        | 8      | Nadam     | 0.0653 | 0.2597   | 11.003     |
| **Baseline2 Model**  | 16         | 3e-5          | 0.10    | 1e-5        | 10     | Adam      | 0.0544 | 0.2237   | 21.269     |
| **Trial Baseline**   | 8          | 5e-5          | –       | –           | 3      | Adam      | 0.0247 | 0.1925   | 21.523     |

🧾 Files

FinalModel.h5 – Best performing model (Nadam, 30 epochs)

PremiumImproved.h5 – High-speed optimized version

Baseline2Model.h5 – Intermediate Adam model

TrialBaseline.h5 – Initial test configuration

README.md – This documentation
