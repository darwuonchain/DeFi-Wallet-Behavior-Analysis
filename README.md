#  DeFi Wallet Behavior Analysis  

### An On-Chain Behavioral Segmentation of DeFi Wallets  

---

##  1. Project Overview  

This project analyzes DeFi wallet activity to uncover distinct behavioral patterns using on-chain data and machine learning techniques.  

By applying clustering and anomaly detection, wallets are segmented into meaningful groups based on transaction frequency, volume, and protocol interaction.

---

##  2. Research Objectives  

- Segment wallets into distinct behavioral groups  
- Differentiate traders, holders, and bots  
- Detect abnormal (bot-like) activity  
- Understand how transaction patterns define wallet behavior  

---

##  3. Data Sources  

- Dune Analytics (primary source)  
- Aggregated wallet-level transaction data  

---

##  4. Blockchains Analyzed  

- Ethereum  
- Polygon  

---

##  5. Stablecoins Tracked  

- USDT  
- USDC  
- DAI  

---

##  6. Dataset Structure  

| Feature | Description |
|--------|------------|
| wallet | Wallet address |
| tx_count | Total transactions |
| total_volume | Total transaction value |
| avg_tx_value | Average transaction value |
| active_days | Wallet lifespan |
| protocols_used | Number of protocols used |
| chain | Blockchain network |

---

##  7. Project Workflow  

### 🔹 Phase 1 — Data Cleaning & Preparation  
- Removed duplicates and missing values  
- Standardized formats and ensured numeric consistency  
- Applied wallet validation and logical filtering  

---

### 🔹 Phase 2 — Feature Engineering  
- Created behavioral metrics (transaction intensity)  
- Applied log transformation to handle skewed distributions  

---

### 🔹 Phase 3 — Clustering (K-Means)  
- Applied KMeans clustering  
- Used Elbow Method to determine optimal K  

**Key Finding:**

K = 3  

Clusters:
- Traders  
- Holders  
- Bots  

---

### 🔹 Phase 4 — PCA Visualization  
- Reduced dimensions using PCA  
- Visualized behavioral separation  

**Insight:** Clear structural separation of wallet behaviors  

---

### 🔹 Phase 5 — Anomaly Detection  
- Applied Isolation Forest  

**Result:** ~5% anomalous wallets detected  

---

##  8. Wallet Personas  

### 🔵 Traders  
- High transaction frequency  
- Moderate transaction value  
- Multi-protocol usage  

### 🟢 Holders  
- Low transaction frequency  
- High-value transactions  
- Long-term holding behavior  

### 🔴 Bots  
- Extremely high frequency  
- Very low transaction value  
- Repetitive automated behavior  

---

##  Key Behavioral Insight  

- Frequency → Bots  
- Value → Holders  
- Balanced → Traders  

---

##  9. Visualizations  

- Elbow Method  
- PCA Clusters  
- Anomaly Detection  
- Cluster Comparison  

---

##  10. Tools & Technologies  

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Jupyter Notebook  
- Seaborn (optional for EDA)  

---

##  11. Applications  

- Fraud and bot detection in DeFi  
- Wallet segmentation for analytics platforms  
- Risk scoring systems  
- Blockchain behavioral intelligence  
- Market behavior analysis  

---

##  12. Project Structure  

```bash
project/
│
├── data/              # Raw & processed datasets
├── notebooks/         # Jupyter notebooks
├── visuals/           # Generated charts & plots
├── src/               # Scripts (cleaning, modeling)
├── README.md          # Project documentation
└── requirements.txt   # Dependencies

##  13. Conclusion  

This project demonstrates that DeFi wallet behavior can be effectively segmented using machine learning techniques.  

Clustering, PCA, and anomaly detection reveal structured behavioral patterns that reflect real-world usage of decentralized finance systems.  

---

##  14. Final Insight  

On-chain transaction behavior is highly structured and measurable, enabling clear separation between human-driven and automated wallet activity in DeFi ecosystems.  

This makes machine learning a powerful tool for understanding financial behavior, detecting anomalies, and classifying wallet personas in decentralized systems.
