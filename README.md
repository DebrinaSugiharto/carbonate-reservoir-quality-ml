# Integrated Geophysical & Machine Learning Workflow for Carbonate Reservoir Quality Assessment

## Overview
This repository presents an integrated geophysical workflow for evaluating carbonate reservoir quality using well log data, fuzzy logic, and neural network modeling. The work reflects practical subsurface interpretation experience and focuses on developing an interpretable, geology-driven decision-support framework.

---

## Purpose
- Translate well log responses into a **reservoir quality indicator** suitable for heterogeneous carbonate reservoirs  
- Handle **gradual facies and property transitions** using fuzzy logic rather than rigid cutoffs  
- Capture **non-linear relationships** between logs and reservoir quality using neural networks  
- Support **integrated asset team** studies and field development planning  

---

## Workflow Summary

### 1. Well Log Analysis
- Input logs: **GR, RHOB, NPHI, DT**
- Logs are interpreted based on their geological meaning in carbonate systems

  <img width="839" height="585" alt="image" src="https://github.com/user-attachments/assets/a1fec02f-5648-4e0d-95b3-614285908911" />


### 2. Fuzzy Reservoir Quality Index (RQI)
- Continuous reservoir quality scale (0–1)
- Cutoffs are used as **soft geological references**
- Designed to reflect subsurface uncertainty and facies transitions

  <img width="408" height="251" alt="image" src="https://github.com/user-attachments/assets/06af1efa-89e3-4e16-ba2c-3a1d46b6fdff" />


### 3. Dimensionality Reduction (PCA)
- Identifies dominant geological drivers
- Reduces redundancy while preserving meaningful variance

  <img width="327" height="171" alt="image" src="https://github.com/user-attachments/assets/173c735b-f1fb-4423-94e8-77990ee634f8" />

The PCA results indicate that the first principal component (PC1) explains approximately 80% of the total variance in the well log data, while the second principal component (PC2) accounts for an additional ~10%. This means that over 90% of the geological information contained in the original multi-dimensional log space (GR, RHOB, NPHI, and DT) can be effectively represented by just two components.

From a geophysical perspective, PC1 captures the dominant rock property control, primarily associated with porosity-related responses and reservoir versus tight carbonate contrast. PC2 reflects secondary heterogeneity, which may be related to facies variation, diagenetic effects, or subtle changes in pore structure commonly observed in carbonate reservoirs.

This result demonstrates that the dataset is governed by a small number of meaningful geological drivers, allowing dimensionality reduction without significant information loss. Such simplification is particularly valuable for integrated reservoir studies and field development planning, as it enables robust interpretation while avoiding unnecessary model complexity.

### 4. Neural Network Modeling (MLP)
- Multi-Layer Perceptron (MLP) neural network
- Used as a **pattern-recognition tool**, not a black-box predictor

  <img width="408" height="224" alt="image" src="https://github.com/user-attachments/assets/87391ce4-d27f-4f96-8003-52669c8ed6b1" />

  An R² of 0.9 indicates that the neural network captures the dominant non-linear relationships between geophysical logs and reservoir quality, making it a reliable decision-support tool when used alongside geological interpretation

  <img width="458" height="470" alt="image" src="https://github.com/user-attachments/assets/a64ff2ad-01c4-4e22-bcc7-0384849a26d1" />
  <img width="394" height="547" alt="image" src="https://github.com/user-attachments/assets/aa8feacc-1359-42a1-a99b-776d6f23014d" />
  <img width="351" height="194" alt="image" src="https://github.com/user-attachments/assets/61efb0d8-0342-4ce1-ad2c-35e56fbbb54b" />

  The neural network predicts the fuzzy reservoir quality index with high consistency, confirming that the dominant non-linear relationships in the log data are well captured. The predicted RQI aligns closely with the fuzzy-based interpretation, reinforcing its use as a decision-support tool rather than a standalone classifier.

---

## Key Observations
- Reservoir quality variability is largely controlled by a limited number of geological factors
- Neural network predictions align well with fuzzy-based interpretation
- Depth-based validation confirms geologically consistent model behavior

---

## Geological Context
- Conceptually aligned with **Middle Eastern carbonate reservoirs**
- Accounts for complex porosity systems and diagenetic effects
- Designed for environments where uncertainty must be managed, not ignored

---

## Author

Debrina Silviana Dewi Sugiharto
Senior Geophysicist (Tunu+SisiNubi Mahakam) + Data Scientist
