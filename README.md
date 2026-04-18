# 📘 DeFiPy: Python SDK for On-chain Analytics

**A quantitative and computational guide to decentralized finance using Python.**

*DeFiPy: Python SDK for On-chain Analytics* accompanies the open-source analytics framework [**DeFiPy**](https://defipy.org) and provides a structured, reproducible foundation for DeFi modeling, simulation, and risk analysis. It unifies the mathematical, programmatic, and architectural components of decentralized finance into an executable, open research framework.

---

## 🧭 Overview

This repository contains the **Jupyter notebooks** for the *DeFiPy TextBook* which is a comprehensive technical reference for the `defipy` ecosystem.

The book introduces:

- **DeFi architecture** – infrastructure, EVM/ABI/JSON-RPC connectivity  
- **AMM mathematics** – constant-product, Balancer, and StableSwap invariants  
- **Analytics and risk modeling** – impermanent loss, expected value, variance, stationarity  
- **Event-driven pipelines** – Web3-based feed handling via `web3.py` and `web3scout`  
- **Agent-based simulation** – supervisory and transition-matrix modeling of DeFi systems  

---

## 🧩 Ecosystem

**DeFiPy** is the root analytics package, composed of three major submodules:

| Module | Description |
|:-------|:-------------|
| [`uniswappy`](https://github.com/defipy-devs/uniswappy) | Uniswap-focused invariant and tick-math analytics |
| [`balancerpy`](https://github.com/defipy-devs/balancerpy) | Balancer-style multi-asset pool invariants and weighting logic |
| [`stableswappy`](https://github.com/defipy-devs/stableswappy) | Curve-style StableSwap invariant and slippage analysis |

DeFiPy integrates seamlessly with **[`web3scout`](https://github.com/defipy-devs/web3scout)**, which is a lightweight extension of `web3.py` that provides efficient on-chain data fetching and event monitoring for analytics pipelines.

---

## 🧱 Repository Structure

```
defipy-book/
├─ notebooks/                # One Jupyter notebook per chapter (chapter1.ipynb … chapter9.ipynb)
├─ LICENSE                   # Apache 2.0 License
└─ README.md                 # This file
```

The full Jupyter notebook suite for all chapter examples lives in the [**defipy-book/notebooks**](https://github.com/defipy-devs/defipy-book/tree/main/notebooks) directory.

---

## 💻 Companion Notebooks

All executable examples are provided as Jupyter notebooks (one per chapter) in the official [**defipy-book/notebooks**](https://github.com/defipy-devs/defipy-book/tree/main/notebooks) repository.

Each notebook reproduces the code listings from the text and can be run locally or in Colab. After installing DeFiPy (see Installation below), clone the notebooks and launch JupyterLab:

```bash
# Install DeFiPy with full book support (needed for chapter 9)
pip install defipy[book] jupyterlab matplotlib

# Clone notebooks and launch
git clone https://github.com/defipy-devs/defipy-book.git
cd defipy-book/notebooks
jupyter lab
```

> **Note:** Chapters 1–8 work with the core install (`pip install defipy`). Only chapter 9 (*Building Autonomous DeFi Agents*) requires the `[book]` extra, which pulls in `web3scout` for on-chain integration.

### Setting Your RPC Endpoint

To run the on-chain examples in this repository, you’ll need a reliable Ethereum JSON-RPC endpoint. The easiest option is to create a free [Infura](https://www.infura.io/) account and generate a project endpoint. Infura provides HTTPS and WebSocket gateways to Ethereum (and other chains), and integrates seamlessly with Web3.py. 

To set one up you can visit [Infura](https://www.infura.io/); once you sign in:

* Create a new Web3 project
* Select Ethereum as the network
* Copy your HTTPS endpoint, which will look like:

```bash
https://mainnet.infura.io/v3/<YOUR_API_KEY>
```

---

## 🚀 Installation

DeFiPy is installed via pip. There are two install options depending on which chapters you plan to run.

### Core install (chapters 1–8)

For the mathematical, analytical, and simulation chapters — which use only DeFiPy's core packages (`uniswappy`, `balancerpy`, `stableswappy`):

```bash
pip install defipy
```

### Book install (all chapters, including chapter 9)

Chapter 9 — *Building Autonomous DeFi Agents* — uses live chain integration via `web3scout`. To run these examples, install the `[book]` extra:

```bash
pip install defipy[book]
```

This adds `web3scout` on top of the core install, providing the chain event monitoring, ABI loading, and token-fetching utilities that chapter 9's agents require.

### Python version

DeFiPy requires **Python 3.10 or later**. Tested through Python 3.14.

### System libraries for gmpy2

`defipy` depends on `gmpy2` for high-precision arithmetic in StableSwap math. `gmpy2` requires the GMP, MPFR, and MPC system libraries to be installed *before* running `pip install`:

**macOS (Homebrew):**
```bash
brew install gmp mpfr libmpc
```

**Linux (Debian / Ubuntu):**
```bash
sudo apt install libgmp-dev libmpfr-dev libmpc-dev
```

### Jupyter

To run the notebooks you'll also need JupyterLab and a plotting library:

```bash
pip install jupyterlab matplotlib
```

---

## 📖 Citation

If you use this book or its code in your research or coursework, please cite:

```
Moore, I. (2025). DeFiPy: Python SDK for On-chain Analytics.
DeFiPy.org, Apache-2.0.
```

---

## 🪶 License

Licensed under the **Apache License, Version 2.0** (the “License”); you may not use this file except in compliance with the License. You may obtain a copy at:

> http://www.apache.org/licenses/LICENSE-2.0

All examples, text, and notebooks are distributed on an “AS IS” basis, without warranties or conditions of any kind.

---

## 🔗 Links

- 📚 [DeFiPy Documentation](https://defipy.org)  
- 💻 [DeFiPy GitHub](https://github.com/defipy-devs/defipy)  
- 🧮 [Companion Notebooks](https://github.com/defipy-devs/defipy-book)  
- ⚙️ [Web3Scout Extension](https://github.com/defipy-devs/web3scout)  

---

**© 2025 defipy-devs / Ian Moore and contributors.**  
Building open, deterministic analytics for decentralized finance.
