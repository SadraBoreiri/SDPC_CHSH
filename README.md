# SPDC-based CHSH Simulation with Noise

This repository contains a Jupyter Notebook implementing simulations related to the paper:

**Bell nonlocality in quantum networks with unreliable sources: Loophole-free postelection via self-testing**  
*Sadra Boreiri, Nicolas Brunner, Pavel Sekatski (2025)*  
[arXiv:2501.14027](https://arxiv.org/abs/2501.14027)

---

## 🔬 About the Implementation

The notebook `SPDC_CHSH_Noisy.ipynb` focuses on the part of the paper where **CHSH violations are studied in the presence of noisy spontaneous parametric down-conversion (SPDC) sources**.  

Specifically, it implements:

- A **numerical model of SPDC photon-pair sources**, including multi-pair emissions and detector inefficiencies.  
- Simulations of the **CHSH inequality violation** under realistic noise conditions.  
- Analysis of how **post-selection of conclusive events** (discarding no-clicks) affects the observed correlations.  

This reproduces the numerical study in the paper showing how CHSH violations can still be observed in a loophole-free way, even when the sources are unreliable.

---

## ⚙️ Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
