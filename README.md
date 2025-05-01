# 🚀 Multi-Label Learning with Incomplete Label Assignments

**IE506 Course Project | Team SS**  
_Sandipan Mondal (24N0457) & Shoumik Das (24N0458)_  
_Guided by Prof. Balamurugan Palaniappan_

---

## 📋 Project Overview

This project addresses the problem of **multi-label classification with incomplete label assignments**, where missing labels can degrade performance. We implemented a framework that:

- ✅ Estimates true label sets using **PU (Positive-Unlabeled) Stochastic Gradient Descent (SGD)**.
- ✅ Leverages **stacked models** to capture label correlations and boost classification accuracy.

---

## 🔬 Problem Statement

- **Challenge:** In many large-scale datasets, some true labels are missing (unlabeled positives), leading to misclassification when these are treated as negatives.
- **Objective:** Develop a method to handle missing labels and exploit label correlations to improve multi-label classification.

---

## 🛠️ Approach

1. **Handling Missing Labels:**
   - Implemented PU learning using logistic regression with SGD.
   - Estimated the probability that a true label is marked (Elkan & Noto’s method).

2. **Label Correlation:**
   - Applied **stacking models** to incorporate inter-label dependencies across multiple levels.

3. **Evaluation:**
   - Tested on the **RCV1 dataset**.
   - Performed experiments with varying missing label rates (0.4 to 0.8).

---

## 📈 Results

Our method outperformed the baseline paper's F1 scores consistently:

| Missing Rate | Paper F1 | Obtained F1 |
|--------------|----------|-------------|
| 0.4          | 0.74     | 0.7951      |
| 0.5          | 0.71     | 0.7848      |
| 0.6          | 0.67     | 0.7503      |
| 0.7          | 0.62     | 0.7019      |
| 0.8          | 0.55     | 0.5937      |

---

## 🧪 Experiments

- **Dataset:** RCV1 (Reuters Corpus Volume I)
- **Tools & Libraries:**
  - Python (Jupyter Notebook)
  - NumPy, SciPy, Scikit-learn
- **Key Functions:**
  - `estimate_c_per_label`
  - `pu_logistic_loss_sgd_binary`
  - `cross_validation_predictions`
  - `mpu_train` and `mpu_predict`
  - `simulate_incomplete_labels`
  - `micro_f1_score`

---


## 🚀 Future Directions

- Integrate **deep learning** (CNNs/Transformers) for richer feature extraction.
- Add **active learning** to selectively label uncertain data points.
- Explore **graph-based models** to capture higher-order label dependencies.
- Enhance scalability with **GPU/distributed computing**.

---

## 🤝 Acknowledgements

- [Kong et al., 2014](https://epubs.siam.org/doi/epdf/10.1137/1.9781611973440.105)
- [Elkan & Noto, 2008](https://cseweb.ucsd.edu/~elkan/posonly.pdf)
- [Manik Varma et al., 2010](http://manikvarma.org/pubs/hariharan10.pdf)

---

## 💬 Contact

For queries or collaboration:  
📧 Sandipan Mondal & Shoumik Das (IIT Bombay)
