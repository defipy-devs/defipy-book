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

DeFiPy integrates seamlessly with **[`web3scout`](https://github.com/defipy-devs/web3scout)**, which is a lightweight extension of `web3.py` that provides efficient on-chain data fetching  
and event monitoring for analytics pipelines.

---

## 🧱 Repository Structure

```
defipy-book/
├─ notebooks/                # Code examples per chapter (lightweight versions)
├─ env/                      # Environment and dependency files
│  ├─ requirements.txt
│  └─ environment.yml
├─ LICENSE                   # Apache 2.0 License
└─ README.md                 # This file
```

The full Jupyter notebook suite for all chapter examples lives in the [**defipy-book-notebooks**](https://github.com/defipy-devs/defipy-book-notebooks) repository.

---

## 💻 Companion Notebooks

All executable examples are provided as Jupyter notebooks (one per chapter) in the official [**defipy-book-notebooks**](https://github.com/defipy-devs/defipy-book-notebooks) repository.

Each notebook reproduces the code listings from the text and can be run locally or in Colab. A simple clone command:

```bash
git clone https://github.com/defipy-devs/defipy-book.git
cd defipy-book/notebooks
jupyter lab
```

For on-chain examples, set your RPC endpoint:

```bash
export WEB3_RPC_URL="https://<provider>/<api-key>"
```

---

## 🧮 Dependencies

DeFiPy and its examples require Python 3.10 or later and the following core packages:

```
defipy
gmpy2
pandas
numpy
matplotlib
web3
jupyterlab
```

Ensure GMP, MPFR, and MPC system libraries are installed prior to `gmpy2`.

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
