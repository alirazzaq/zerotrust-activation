# ZeroTrust Activation (ZTA) 🔒

**A cybersecurity-inspired, dual-gate activation function for deep neural networks**

[![Paper](https://img.shields.io/badge/Paper-arXiv-green.svg)](https://arxiv.org/abs/your-arxiv-url) [![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

---

## Overview

ZeroTrust Activation (ZTA) is a novel generic and robust activation function for neural networks, inspired by the "Zero Trust" paradigm in cybersecurity. It combines a learnable sigmoid ("trust verification") and tanh ("boundary enforcement") gate:

\[
\text{ZTA}(x;\alpha, \beta) = x \cdot \sigma(\alpha x) \cdot \tanh(\beta x)
\]

- **Learnable parameters:** $\alpha$ and $\beta$ are trust-levels optimized by backpropagation.
- **Compatible** with CNNs, ViTs, MLPs, and more.
- **Outperforms** ReLU, GELU, Mish, Swish on accuracy, robustness, and gradient flow.
- **Built for reproducible research and real deployment.**

> This repo contains code, PyTorch modules, training scripts, and evaluation tools to reproduce the results from the paper.

---

## Key Features

- 📈 **State-of-the-art results:** 7 datasets, 9 architectures, 10+ baselines.
- 🔐 **Adversarial robustness:** PGD-20 & FGSM attack hooks.
- 🏆 **Gradient stability:** Zero dead neurons, healthy gradients in all layers.
- ⚡ **Efficiency:** Minimal FLOPs and latency increase.
- 📊 **Publication-ready Figures:** Automation for all paper plots.
- 🧪 **Reproducibility:** All hyperparameters, ablations, and statistical significance scripts provided.

git clone https://github.com/yourusername/zerotrust-activation.git
cd zerotrust-activation
pip install -r requirements.txt


Requirements:
- Python 3.8+
- PyTorch >= 1.9
- torchvision
- torchattacks (for adversarial evaluation)
- matplotlib, seaborn, scikit-learn, tqdm

---

## Usage

### 1. Use ZTA in Your Model

from zta import ZeroTrustActivation
layer = ZeroTrustActivation(alpha_init=1.0, beta_init=1.0)

---

## Installation

