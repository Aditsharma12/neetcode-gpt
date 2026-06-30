# 🤖 NeetCode GPT

> **Building GPT from scratch — one concept at a time.**

A complete implementation of a **Generative Pre-trained Transformer (GPT)** built from scratch while completing the **NeetCode Machine Learning Course**. The goal of this repository is to understand every building block of modern Large Language Models instead of treating them as black boxes.

---

# ✨ Features

* 🧠 Neural Networks from scratch
* 📚 Tokenization (Character & BPE)
* 🔤 Vocabulary Construction
* 🔢 Embeddings & Positional Encoding
* ⚡ Self Attention
* 👥 Multi-Head Attention
* 🏗️ Transformer Blocks
* 🚀 GPT Language Model
* ✍️ Autoregressive Text Generation

---

# 🏛️ Project Architecture

```mermaid
flowchart LR

A[Raw Text Corpus]
B[Tokenizer]
C[Vocabulary]
D[Embedding Layer]
E[Positional Encoding]
F[Transformer Blocks]
G[Language Model Head]
H[Next Token Prediction]
I[Generated Text]

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> H
H --> I
```

---

# 🧠 GPT Pipeline

```mermaid
flowchart TD

A[Input Text]
B[Tokenization]
C[Embedding]
D[Add Positional Encoding]
E[Transformer Layer 1]
F[Transformer Layer 2]
G[...]
H[Final LayerNorm]
I[Linear Projection]
J[Softmax]
K[Predicted Token]

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> H
H --> I
I --> J
J --> K
```

---

# 🔄 Training Workflow

```mermaid
flowchart LR

Dataset --> Tokenizer
Tokenizer --> InputTokens
InputTokens --> GPT
GPT --> Logits
Logits --> CrossEntropyLoss
CrossEntropyLoss --> Backpropagation
Backpropagation --> Optimizer
Optimizer --> GPT
```

---

# ⚙️ Transformer Block

```mermaid
flowchart TD

A[Input Embeddings]

A --> B[LayerNorm]
B --> C[Multi Head Attention]
C --> D[Residual Connection]

D --> E[LayerNorm]
E --> F[Feed Forward Network]
F --> G[Residual Connection]

G --> H[Output]
```

---

# 📂 Repository Structure

```text
neetcode-gpt/
│
├── tokenizer/
├── datasets/
├── embeddings/
├── attention/
├── transformer/
├── gpt/
├── training/
├── inference/
├── utils/
├── notebooks/
├── requirements.txt
└── README.md
```

---

# 📖 Concepts Covered

## Neural Networks

* Forward Propagation
* Backpropagation
* Gradient Descent
* Activation Functions
* Loss Functions

---

## Natural Language Processing

* Character Tokenization
* Byte Pair Encoding (BPE)
* Vocabulary Building
* Embedding Layers

---

## Transformers

* Self Attention
* Scaled Dot Product Attention
* Multi Head Attention
* Layer Normalization
* Feed Forward Networks
* Residual Connections
* Positional Encoding

---

## GPT

* Decoder-only Transformer
* Autoregressive Generation
* Cross Entropy Loss
* Causal Masking
* Next Token Prediction

---

# 🛠️ Installation

```bash
git clone https://github.com/Aditsharma12/neetcode-gpt.git

cd neetcode-gpt

pip install -r requirements.txt
```

---

# 🚀 Usage

Train the model

```bash
python train.py
```

Generate text

```bash
python generate.py
```

---

# 🔍 How GPT Generates Text

```mermaid
sequenceDiagram

participant User
participant Tokenizer
participant GPT
participant Softmax

User->>Tokenizer: Input Prompt
Tokenizer->>GPT: Tokens
GPT->>Softmax: Logits
Softmax->>GPT: Next Token
GPT->>Tokenizer: Append Token
Tokenizer->>User: Generated Text
```

---

# 🎯 Learning Objectives

This repository focuses on understanding:

* Transformer internals
* Attention mechanisms
* Language model training
* Tokenization algorithms
* Building GPT from first principles
* Modern LLM architecture

---

# 📚 References

* NeetCode Machine Learning Course
* Attention Is All You Need (2017)
* GPT-2 (OpenAI)
* The Illustrated Transformer

---

# ⭐ Repository Goals

This project is intended as an educational implementation for anyone interested in learning how modern Large Language Models are built from scratch.

If you find this repository useful, consider giving it a ⭐.

---

# 📜 License

This project is released for educational purposes.
