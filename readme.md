# 🛡️ AI & Cybersecurity

A machine learning and deep learning project exploring AI-based approaches for malware classification, network anomaly detection, and SSH attack analysis.

<br>

## 📌 Overview

This project applies different Artificial Intelligence techniques to cybersecurity problems, including:

<br>

- Classifying malware through API call sequences
- Detecting anomalies in network traffic
- Comparing supervised and unsupervised learning approaches
- Analyzing SSH and Bash command sequences
- Mapping malicious behavior to MITRE tactics
- Identifying recurring attack patterns

The project focuses on comparing different data representations and AI architectures to understand how they affect cybersecurity detection performance.

## 🦠 Malware Classification

Malware and benign samples are analyzed through sequences of API calls.

<br>

Different approaches were implemented and compared:

- Frequency-based representations
- Feed-Forward Neural Networks (FFNN)
- Learnable embeddings
- Recurrent Neural Networks (RNN)
- Bidirectional RNN
- LSTM
- Graph Neural Networks (GNN)

The GNN experiments include:

<br>

- GCN
- GraphSAGE
- GAT

Sequential models demonstrated the importance of preserving API call ordering, while GraphSAGE achieved the best performance among the evaluated GNN architectures.

## 🔍 Network Anomaly Detection

Network traffic is analyzed to distinguish normal behavior from attacks such as:

<br>

- Denial of Service (DoS)
- Probe
- Remote-to-Local (R2L)

Multiple anomaly detection techniques were explored:

<br>

- One-Class SVM
- Autoencoders
- PCA + One-Class SVM
- Autoencoder embeddings + One-Class SVM
- K-Means
- DBSCAN
- t-SNE

The experiments highlight the importance of training anomaly detection models on clean normal traffic and the trade-offs introduced by dimensionality reduction.

## 🤖 SSH & Bash Attack Analysis

Transformer-based models are used to analyze SSH sessions and classify Bash commands according to attacker behavior.

<br>

The project compares:

- BERT
- UniXcoder
- BERT trained from scratch
- Full and partial fine-tuning strategies

UniXcoder achieved the best results, reaching a **Macro F1 score of 0.7046**, compared with **0.5506 for fine-tuned BERT**.

The results demonstrate the advantage of code-oriented pre-training when analyzing shell commands and other code-like cybersecurity data.

## 🎯 MITRE Tactic Classification

SSH commands are classified according to their context and associated attacker behavior.

<br>

Examples include:

- Discovery
- Execution
- Persistence
- Defense Evasion

The experiments show that individual commands cannot always be associated with a single tactic. Their meaning depends on the surrounding SSH session and execution context.

## 🔗 Attack Fingerprinting

Predicted tactic sequences are combined into behavioral fingerprints representing SSH sessions.

<br>

These fingerprints can be used to:

- Identify recurring attacker behavior
- Detect high-frequency attack patterns
- Track emerging behavioral sequences
- Highlight potential automated attack campaigns

## 🛠️ Technologies

**Languages:** Python

**Machine Learning:** PyTorch, scikit-learn

**Data Analysis:** Pandas, NumPy

**Visualization:** Matplotlib, Seaborn, t-SNE

**Deep Learning:** FFNN, RNN, Bi-RNN, LSTM, Autoencoders

**Graph Learning:** GCN, GraphSAGE, GAT

**Transformers:** BERT, UniXcoder, Hugging Face Transformers

**Anomaly Detection:** One-Class SVM, PCA, K-Means, DBSCAN

## 🎯 Key Features

- Malware classification from API call sequences
- Sequential behavior modeling with RNNs and LSTMs
- Graph-based malware analysis with GNNs
- Network intrusion and anomaly detection
- Dimensionality reduction with PCA and Autoencoders
- SSH/Bash analysis with Transformer models
- Context-aware MITRE tactic classification
- Behavioral attack fingerprinting

## 🚀 Future Improvements

- Larger and more balanced training datasets
- Transformer-based modeling of API call sequences
- Advanced GNN architectures
- Improved handling of rare attack classes
- Explainable AI techniques for security predictions
- Real-time intrusion and attack detection
