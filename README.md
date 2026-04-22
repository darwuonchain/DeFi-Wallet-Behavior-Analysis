**DeFi Wallet Behavior Analysis**

**An On-Chain Behavioral Segmentation of DeFi Wallets**

1.**Project Overview**

This project analyzes DeFi wallet activity to uncover distinct behavioral patterns using on-chain data and machine learning techniques.
By applying clustering and anomaly detection, wallets are segmented into meaningful groups based on transaction frequency, volume, and protocol interaction.

2.**Research Objectives**

Segment wallets into distinct behavioral groups

Differentiate traders, holders, and bots

Detect abnormal (bot-like) activity

Understand how transaction patterns define wallet behavior

3.	**Data Sources**

Dune Analytics (primary source)

Aggregated wallet-level transaction data

4.	**Blockchains Analyzed**

Ethereum

Polygon

5.	**Stablecoins Tracked**

USDT

USDC

DAI

6.	**Dataset Structure**

Each wallet-level record includes:

Feature                                                  Description
wallet                                                Wallet address
tx_count                                              Total transactions
total_volume                                           Total transaction value
avg_tx_value                                         Average transaction value
active_days                                          Wallet lifespan 
protocols_used                                       Number of protocols used 
chain                                               Blockchain network

7.	**Project Workflow**

Phase 1 — Data Cleaning & Preparation

Removed duplicates and missing values

Standardized formats and ensured numeric consistency

Applied wallet validation and logical filtering

**Insight**:

A structured data cleaning pipeline ensures high-quality and reliable blockchain behavioral data.

Phase 2 — Feature Engineering

Selected key behavioral features

Created derived metrics (e.g., transaction intensity)

Applied log transformation to handle skewed distributions

**Insight**:

Log scaling reduces the dominance of extreme values and improves interpretability.

Phase 3 — Clustering (K-Means)

Applied KMeans to segment wallets into clusters

Used the Elbow Method to determine optimal K

**Key Finding**:

K = 3 provides the optimal balance between simplicity and performance

**Interpretation**:

Clusters align with real-world DeFi roles:

Traders

Holders

Bots

**Phase 4 — PCA Visualization**

Reduced feature space using PCA

Visualized clusters in 2D

**Insights**:

Clear separation between wallet types

Behavioral intensity drives clustering

Outliers indicate abnormal or automated activity

**Critical Insight**:

A small subset of wallets behaves fundamentally differently — likely bots or high-frequency systems.

Phase 5 — Anomaly Detection

Applied Isolation Forest to detect abnormal behavior

**Result**:

~5% of wallets identified as anomalous

**Interpretation**:

These wallets exhibit:

Extremely high transaction frequency

Irregular transaction patterns

Non-organic behavior

Phase 6 — Key Insights

Bots dominate high-frequency, low-value transactions

Traders interact across multiple protocols

Holders exhibit low-frequency, high-value behavior

A small subset of wallets drives the majority of activity

8.**Wallet Personas**

🔵 Traders

Behavior:

High transaction frequency

Moderate transaction value

Multi-protocol usage

**Interpretation**:

Active DeFi participants engaging in frequent trading and liquidity activities

🟢 Holders

Behavior:

Low transaction frequency

High-value transactions

Long-term activity

**Interpretation**:

Investment-oriented wallets holding assets over time

🔴 Bots

Behavior:

Extremely high transaction frequency

Very low transaction value

Repetitive patterns

**Interpretation**:

Automated systems executing algorithmic or high-frequency transactions

Key Behavioral Insight

Frequency-driven wallets → Bots

Value-driven wallets → Holders

Balanced activity → Traders

9.	Visualizations

Elbow Method

PCA Clusters

Anomaly Detection

Cluster Comparison

10. **Project Structure**

project/
│
├── data/              # Raw & processed datasets
├── notebooks/         # Jupyter notebooks
├── visuals/           # Charts & plots
├── src/               # Data processing & modeling scripts
├── README.md          # Documentation
└── requirements.txt   # Dependencies

11.	**Tools & Technologies**

Python

Pandas

NumPy

Scikit-learn

Matplotlib

12.**Applications**

Fraud and bot detection

DeFi user segmentation

Risk scoring systems

Blockchain behavioral analytics

13.	**Conclusion**

This project demonstrates that DeFi wallet behavior can be effectively segmented using machine learning.
Clustering, PCA, and anomaly detection reveal structured and interpretable behavioral patterns within on-chain activity.

14.	**Final Insight**

On-chain transaction behavior is structured and measurable, enabling clear distinction between human-driven activity and automated systems in DeFi ecosystems.


