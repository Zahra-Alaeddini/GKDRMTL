<p align="center">
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License: MIT">
  </a>
  <img src="https://img.shields.io/badge/Python-3.8%2B-orange" alt="Python Version">
</p>


# GKD2RMTL: A Multi-Task Learning and Knowledge Distillation Framework for Efficient Graph-Based Drug Repurposing

**GKD2RMTL** is a graph-based **teacher-student** framework designed for **multi-task learning** on a customized **Biomedical Knowledge Graph (BKG)**. It aims to enhance **drug repurposing** by predicting a variety of biomedical relationships using graph neural networks and knowledge distillation techniques.

## 🧠 Overview

The **teacher model** is a deep, expressive architecture built with:
- Multi-layer **GraphSAGE**
- **Leaky ReLU** activations
- **Dropout regularization**
- **Task-specific output heads**

It is employed to predict:
- 🧪 **Drug-Disease Associations**  
- 🧬 **Drug-Gene Binding Interactions**  
- 💊 **Drug Similarity**  
- 🧫 **Disease-Gene Associations**

<p align="center">
  <img src="https://github.com/user-attachments/assets/e106ff4e-465f-42ec-938f-0c823ad5be02" alt="GKD2RMTL Architecture" width="600"/>
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
- **Adaptive negative sampling** improves performance on sparse graphs

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
