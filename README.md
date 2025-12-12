# EffortGNN  
Graph Neural Networks for Agile Story Point Estimation

EffortGNN is a framework for estimating story points using Graph Neural Networks (GNNs) applied over semantic graphs built from textual issue descriptions. It supports within-project and cross-project evaluation, multiple model variants, and reproducible multi-run experiments.

---

## Overview
- SBERT (all-MiniLM-L6-v2) embeddings (384-d)  
- k-NN semantic graph construction (k = 4, cosine similarity)  
- Three GNN architectures:  
  - GraphSAGE  
  - GCN  
  - GAT (2-head attention)  
- Evaluation modes:  
  - **Within-project** (70/15/15 split)  
  - **Cross-project** (train on many projects; test on held-out project)  
- Controlled multi-run evaluation (10 runs with `mean ± std`)  
- Automatic metric logging

---

The system is fully aligned with the methodology described in the associated research paper:
Combining Textual Embeddings and Graph Neural Networks for Agile Software Effort Estimation