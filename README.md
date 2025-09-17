# SPDC-based CHSH Simulation with Noisy/Unreliable Sources

This repository contains a Jupyter Notebook that numerically studies **CHSH violations** using SPDC-inspired sources under realistic noise and post-selection. It accompanies the paper:

**Bell nonlocality in quantum networks with unreliable sources: Loophole-free postelection via self-testing**  
Boreiri, Brunner, Sekatski (2025) — [arXiv:2501.14027](https://arxiv.org/abs/2501.14027)

---

## 📖 Short Summary of the Paper

The paper investigates **Bell nonlocality in quantum networks with unreliable sources**, i.e. sources that may **fail to emit photons** (as in SPDC, where vacuum events occur).  
Discarding inconclusive outcomes normally risks opening the **detection loophole**, but the authors show that:

- If measurements satisfy **fair-sampling**, then **post-selection remains loophole-free**.  
- **Saturation of the Finner inequality** can be used as a **self-test**, certifying fair-sampling directly from observed data.  
- This enables **device-independent randomness generation** even with imperfect sources.  

👉 In this notebook we consider the **Bell scenario (CHSH test)** and show that post-selection can lead to **higher CHSH violations** and therefore a **higher certified randomness rate** compared to the non-post-selected data.

---

## 🔬 About the Implementation

**File:** `SPDC_CHSH_Noisy.ipynb`

This notebook reproduces part of the numerical analysis from the paper: **CHSH violations with noisy SPDC sources**.  

It implements:

- **A numerical model of SPDC photon-pair sources**, including:
  - **Vacuum events** (source emits nothing),
  - **Multi-pair emissions** (SPDC producing more than one pair),
  - **Detector inefficiencies** (`eta`),
  - **Dark counts** (`p_dc`).
- Compute **maximum CHSH score** as a function of a source “brightness” parameter `T` by optimizing local measurement angles, with two modes:
  - **Standard (no post-selection)** — computes CHSH directly from the full distribution.
  - **Post-selected** — conditions on a conclusive event on Alice and recomputes CHSH on the conditional distribution (Note that this is the same as discarding the fully-inconclusive block when `eta=1` and `p_dc=0`).
 
- A lower bound on the **randomness rate** derived from the CHSH value and post-selection rate.


This illustrates the core idea: even with unreliable sources and realistic noise, **loophole-free CHSH violations** (and hence certified randomness) are achievable.

---

## ⚙️ Requirements

- numpy  
- scipy  
- matplotlib  
