
# Machine Learning Fundamentals 

This repository documents my experiments and implementations of **core machine learning fundamentals**, focusing on model capacity, overfitting, and training stability in deep networks.  
All work is based on hands-on coursework using EMNIST and CIFAR-100 datasets.


## Fundamentals Learned

### 1. Overfitting & Model Capacity
- Investigated how **network width (number of units)** and **depth (number of layers)** affect generalisation.  
- Observed that larger models tend to **overfit** small datasets.  
- Implemented and tested regularisation methods:
  - **Dropout**
  - **L1 and L2 penalties**
  - **Label smoothing**

**Key Idea:** Regularisation is essential to control capacity and reduce the generalisation gap.

---

### 2. Vanishing Gradients in Deep Networks
- Analysed **gradient flow** in VGG-08 vs VGG-38 models.  
- Found that very deep networks suffer from the **vanishing gradient problem (VGP)**, preventing effective training.  
- Implemented stabilisation techniques:
  - **Batch Normalisation (BN)**
  - **Residual Connections (RC / skip connections)**
  - **BN + RC combined**

**Key Idea:** BN and RC improve gradient propagation, allowing deeper networks to converge and generalise better.

---

## Results Snapshot
- **Overfitting study (EMNIST):**  
  - Dropout and L2 regularisation improved robustness on unseen data.  
- **Vanishing gradient study (CIFAR-100):**  
  - VGG-38 failed to train without fixes.  
  - VGG-38 + BN + RC achieved **60% validation accuracy**, showing stable training and improved performance.

---

## Skills Practiced
- Diagnosing **overfitting** and **vanishing gradients**.  
- Applying **regularisation** (Dropout, L1/L2 penalties, label smoothing).  
- Applying **training stabilisation** (BatchNorm, Residual Connections).  
- Empirical analysis of model behaviour across datasets.  

---

## Takeaway
Machine learning models require more than just adding depth or parameters:  
- **Capacity control** (via width/depth vs. data size) avoids overfitting.  
- **Regularisation** improves generalisation.  
- **BatchNorm and Residual Connections** are critical for training very deep models.  

This repository captures these **fundamental principles** through hands-on experiments.
