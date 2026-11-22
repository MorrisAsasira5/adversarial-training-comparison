# Defending Image Classification Systems Against Evasion Attacks

### A Comparative Study of Adversarial Training Methods

**Morris Asasira A. · S24B23/116 · Uganda Christian University**

A normal image classifier can be fooled by changing an image by an amount too small for a human to notice. This project trains a single residual CNN architecture with three different defenses and attacks every trained model with the same attacks, under identical conditions, so the defenses can be compared directly and fairly.

## What it covers

- **Defenses:** Standard Adversarial Training (SAT), Ensemble Adversarial Training, and TRADES — all using the same CNN architecture on the same dataset (CIFAR-10).
- **Attacks:** FGSM and PGD (white-box), plus transfer (black-box) attacks from an undefended model.
- **Metrics:** clean accuracy, robust (adversarial) accuracy, and attack success rate (ASR), with a focus on the trade-off between clean accuracy, robustness, and training cost.

## Research objectives

1. Implement and train three defenses (SAT, Ensemble AT, TRADES) with the *same* architecture on the *same* dataset for a fair comparison.
2. Test robustness with FGSM and PGD, reporting robust accuracy and attack success rate.
3. Study the trade-offs between clean accuracy, robustness, and training cost.

## Running the notebook

The notebook (`Adversarial_Training_Comparison_ResCNN_final.ipynb`) is written for Google Colab with a GPU:

- Checkpoints and results are saved to an `adv_demo` folder on Google Drive so they survive Colab disconnects. Run outside Colab (e.g. local Jupyter) and a local `adv_demo_local` folder is used instead.
- The attack library `torchattacks` is used as a reference; the notebook also implements its own FGSM and PGD so each step can be read and explained, then checks them against `torchattacks`.
- A GPU is strongly recommended — adversarial training on CPU is not practical.

Run the cells in order, starting from the Imports and Configuration section.

## Research poster

`Research_Poster_A2_Landscape.pdf` is the A2 landscape poster summarizing this project — the defenses compared, the attack setup, and the headline results.
