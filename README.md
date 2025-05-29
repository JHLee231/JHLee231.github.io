# LoRA-RL for Analog Circuit Sizing

This repository accompanies the paper:  
**“LoRA-RL: Low-Rank Adaptation Enables Fast, Transferable Reinforcement Learning for Analog Circuit Optimization”**

---

## 🔍 Overview

LoRA-RL is a parameter-efficient framework for analog transistor sizing.  
Instead of retraining the entire GCN-RL model on every new circuit or process node, we:

- **Pre-train** a GCN-based actor–critic policy on a reference circuit
- **Freeze** all backbone weights
- **Fine-tune** only small low-rank (LoRA) adapters during transfer

---

## 🎯 Goal

Enable **fast and stable** transfer of sizing policies across process nodes or topologies,  
by adapting just a small subspace of the network while preserving learned analog priors.

---

## 📈 Results

- ✅ Up to **8× faster convergence**
- ✅ **Higher or comparable FoM** across four amplifier topologies (A–D)
- ✅ **Reduced SPICE evaluations** during transfer (TSMC 45 nm)

See `figs/` and `logs/` for learning curves and simulation results.

---

## 📂 Repository Layout

