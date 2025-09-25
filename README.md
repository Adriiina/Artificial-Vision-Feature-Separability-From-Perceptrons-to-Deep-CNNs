# Artificial Vision & Feature Separability: From Perceptrons to Deep CNNs

![Python](https://img.shields.io/badge/Python-3.10+-blue) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange) ![Torch](https://img.shields.io/badge/PyTorch-2.x-red) ![License](https://img.shields.io/badge/License-MIT-green)

**Goal.** Explore how **feature separability** evolves from classic linear models (perceptron/logistic) to **CNNs**, using synthetic colors, MNIST, and **EMNIST**.  
**Focus.** Representation geometry (PCA), clustering, linear separability, and **linear probes** on hidden activations.

---

## 🚀 Quickstart

```bash
git clone https://github.com/Adriiina/Artificial-Vision-Feature-Separability-From-Perceptrons-to-Deep-CNNs.git
cd Artificial-Vision-Feature-Separability-From-Perceptrons-to-Deep-CNNs
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements_00.txt  # install others as you run each notebook
Data notes

Colors: place data/colors.csv with R,G,B,label (or L,a,b,label).

MNIST / EMNIST / CIFAR: auto-download via torchvision. The notebooks include an SSL fix.

Large raw data → not committed; outputs go to results/.
📁 Repository structure
.
├── notebooks/
│   ├── 00_intro_features_pca_kmeans.ipynb
│   ├── 01_colors_baselines_prototype_exemplar.ipynb
│   ├── 02_colors_advanced_baselines_logloss.ipynb
│   ├── 03_exemplar_models_gcm.ipynb
│   ├── 04_mnist_logistic_baseline.ipynb
│   ├── 05_perceptron_linear_separability.ipynb
│   └── 06_cnn_emnist_representation_probing.ipynb
├── requirements_00.txt  requirements_01.txt  requirements_02.txt  requirements_03.txt
├── requirements_04.txt  requirements_05.txt  requirements_06.txt
├── data/        # put your CSVs here (not tracked)
├── results/     # figures & small CSVs saved here
├── .gitignore
└── README.md

🧭 Project tour (notebooks)

00 · Intro to Features, PCA & K-Means — PCA + K-Means intuition.
01 · Colors: Baselines, Prototype & Exemplar — Logistic, Prototype, k-NN, GCM.
02 · Colors (Advanced & Log-Loss) — CV on C, log-loss, calibration, ROC-AUC.
03 · Exemplar Models & GCM — (c,p) CV, sensitivity curves, summary CSV.
04 · MNIST Logistic Regression Baseline — C-sweep, ROC-AUC, calibration, error grid.
05 · Perceptron & Linear Separability — mistakes/epoch, margins, logistic compare.
06 · CNN on EMNIST + Representation Probing — PCA of layer activations, linear probes.

🧪 Reproducibility

Notebooks set a seed and create results/. Data-downloading notebooks set:

import os, certifi
os.environ["SSL_CERT_FILE"] = certifi.where()

