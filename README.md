# Qwen3 (14B) Reasoning Conversational Agent

This project demonstrates a conversational reasoning chatbot using the **Qwen1.5-14B-Chat** model from Alibaba’s Qwen family, running on Hugging Face `transformers` and `accelerate`.

## 💡 Overview

This notebook showcases:
- Loading the Qwen1.5 14B model using Hugging Face Transformers.
- Setting up conversational chat format inputs.
- Running local inference using bfloat16 or float16 (depending on device).
- Enabling reasoning with memory-style dialogue inputs.

---

## 🧰 Tech Stack

| Tool/Library   | Purpose                         |
|----------------|----------------------------------|
| Python 3.10+   | Core programming language        |
| PyTorch        | Model execution backend          |
| Transformers   | Hugging Face model APIs          |
| Accelerate     | Multi-device inference support   |
| SentencePiece  | Tokenizer backend                |

---

## 🧠 Model Info

  - Model: Qwen1.5-14B-Chat
  - Source: Hugging Face
  - License: Apache 2.0

## 📄 Datasets
   - OpenMathReasoning-mini (19252 samples)
   - FineTome-100k (100000 samples, subsampled)

## 📘 Performance
   - Trained on Tesla T4 GPU (16GB VRAM)
   - Batch size: 8 (2 per device × 4 gradient accumulation)
   - Training time: ~40 minutes for 30 steps

## 📌 Features

 - Combines mathematical reasoning (OpenMathReasoning dataset) with conversational abilities (FineTome-100k dataset)
 - Uses 4-bit quantization for memory efficiency
 - Implements LoRA adapters for parameter-efficient finetuning
 - Supports both reasoning and chat modes with different temperature settings
 - Export options for GGUF/llama.cpp and 16-bit models

## ✅ Requirements.txt
  - torch>=2.1.0
  - transformers>=4.40.0
  - accelerate>=0.27.0
  - sentencepiece>=0.1.99


## ⚙️ Setup & Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Sayiqajabeen/qwen3-reasoning-chatbot.git
cd qwen3-reasoning-chatbot
