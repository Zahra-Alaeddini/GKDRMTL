<p align="center">
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License: MIT">
  </a>
  <img src="https://img.shields.io/badge/Python-3.8%2B-orange" alt="Python Version">
</p>


# GKDRMTL: Graph-based Knowledge Distillation Framework for Drug Repurposing via Multi-task Learning

**GKDRMTL** is a graph-based framework designed for **multi-task learning** on a customized **Biomedical Knowledge Graph (BKG)**. It aims to enhance **drug repurposing** by predicting a variety of biomedical relationships using graph neural networks and knowledge distillation approaches.

## 🧠 Overview

The **teacher model** is a deep, expressive architecture built with:
- Multi-layer **GraphSAGE**
- **Leaky ReLU** activations
- **Dropout regularization**
- **Task-specific output heads**

It is employed to predict:
- 🧪 **drug-disease associations**  
- 🧬 **disease similarity**  
- 💊 **drug similarity**  
- 🧫 **disease-gene associations**

<p align="center">
  <img width="2738" height="1570" alt="GKDRMTL Architecture" src="https://github.com/user-attachments/assets/b7ba893f-9ffd-45a5-8e4e-8f8d6f5e1010" />  
</p>

The **student model** is lightweight, employing a **single-layer GraphSAGE** with task-specific heads. It learns from the teacher via **knowledge distillation**, using **distillation loss** to transfer knowledge effectively.

## ⚙️ Key Features

✅ Multi-task learning with **task-specific heads**  
✅ **Graph-based knowledge distillation** for compact student models  
✅ **Optimized negative sampling** for imbalanced biomedical graphs  
✅ **Lightweight student architecture** for scalable deployment  
✅ Joint use of **node features**, **edge attributes**, and **GraphSAGE embeddings**

## 📊 Handling Class Imbalance

To address class imbalance in edge prediction tasks:
- **Weighted binary cross-entropy loss** is applied
- **Adaptive hard negative sampling** improves performance on sparse graphs

## 📝 License
This project is licensed under the [MIT License](LICENSE).

## 📬 Contact
For questions, feel free to reach out:

- 👩‍💻 **Zahra Alaeddini**
  
📧 alaeddini.zahra@gmail.com

## 📦 Prerequisites

Make sure you have the following dependencies installed:

```bash
Python >= 3.8  
PyTorch
PyTorch Geometric 
NumPy  
Pandas  
Scikit-learn
