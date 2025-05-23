# GNN-Based Intrusion Detection with Focal Loss and Edge Features

Presented in **International Conference on Web Intelligence and Human-
Machine Interaction (ICWIHI 2025)** organised by R P Sarathy Institute of Technology, Salem, Tamil Nadu, India on 8 April 2025.

This project presents a **Graph Neural Network (GNN)**-based framework for network intrusion detection using the **UNSW-NB15** dataset. Unlike traditional ML/DL approaches that treat network events independently, our system represents them as nodes in a graph and uses **edge attributes** and **Focal Loss** to boost detection performance, particularly for underrepresented attack types.

## 🚀 Highlights

- ⚙️ Graph-based representation of network flows (nodes = events, edges = protocol/service/state relations)
- 📊 Incorporation of **edge features** (e.g., packet similarity, TCP timings) to enhance context
- 📉 Use of **Focal Loss** to handle class imbalance and improve rare attack classification
- 🧠 GCNII-based deep architecture with residuals to avoid over-smoothing
- 📈 High test accuracy (~96.19%) and strong recall for previously hard-to-detect attack classes

## 📂 Dataset

- **UNSW-NB15** (Australian Centre for Cyber Security)
- 9 attack categories + normal traffic
- Preprocessing includes:
  - Removal of IP/port/time features
  - One-hot encoding of categoricals
  - Min-max feature scaling
  - Mapping for binary and multi-class labels

## 🧠 Model Architecture

- Input: Node and edge features
- Feature extractor: Statistical + temporal attributes
- 8-layer GCNII with GELU activation, dropout
- Output: Softmax (multi-class) / Sigmoid (binary)
- Optimizer: Adadelta, Batch Size: 256, Early Stopping: 20 epochs

## 🧪 Evaluation Metrics

| Metric | Value |
|--------|-------|
| Accuracy | 96.19% |
| Balanced Accuracy | 61.28% |
| Macro F1 | 41.3% |
| Weighted F1 | 96.9% |

## 🔧 Requirements

```txt
torch
torch_geometric
numpy
pandas
scikit-learn
matplotlib
seaborn
networkx
```

## 📦 Installation

```bash
git clone https://github.com/your-username/GNN-Intrusion-Detection.git
cd GNN-Intrusion-Detection
pip install -r requirements.txt
```

## 👨‍💻 Authors (B.Tech'25 IGDTUW, Delhi)
- Kanika Kamalhans (kanikamalhans@gmail.com)
- Anushka Gupta (anushka.2210@gmail.com)
- Ayushi (ayushisharma200311@gmail.com)
- Amisha Sharma (amishasharma2778@gmail.com)


