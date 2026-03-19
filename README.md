# 📈 Dividend Capital Simulator

> Find out how much capital you need to live off dividends — Monte Carlo simulation with a clean web interface.

![License](https://img.shields.io/badge/license-MIT-gold) ![HTML](https://img.shields.io/badge/built%20with-HTML%20%2F%20JS-blue)

---

## 🎯 What it does

Enter the **monthly net income** you want to generate from dividends, configure your portfolio parameters, and the simulator calculates — via **Monte Carlo** — how much capital you need across different scenarios (pessimistic, base, optimistic).

---

## ✨ Features

- **Main input**: desired monthly net income
- **Monte Carlo simulation** with 1,000–20,000 iterations
- **3 scenarios**: pessimistic (P5), base (median P50), optimistic (P95)
- **Interactive histogram** of the simulated capital distribution
- Configurable parameters: dividend yield, annual growth, tax rate, volatility
- Runs entirely in the browser — **no installation or dependencies required**

---

## 🚀 How to use it

### Option 1 — directly in the browser
Download `index.html` and open it in any modern browser. No setup needed.

### Option 2 — GitHub Pages (online)
Publish it for free on GitHub Pages by following the instructions in the repository setup guide.

---

## 📁 Project structure

```
dividend-simulator/
├── index.html       # Full app (HTML + CSS + JS in a single file)
├── README.md        # This file
└── LICENSE          # MIT License
```

---

## ⚙️ Parameters
The parameters can be change
--This is an example of how the parameters can be 
| Parameter | Description | Default |
|---|---|---|
| Monthly income | Target monthly net income | €20,000 |
| Time horizon | Simulation period in years | 10 |
| Dividend Yield | Portfolio gross annual yield | 5.0% |
| Annual growth | Expected dividend growth rate | 6.0% |
| Tax rate | Tax rate applied to dividends | 10% |
| Volatility | Standard deviation of growth shocks | 2.0% |
| Simulations | Number of Monte Carlo iterations | 15,000 |

---

## 🧮 Methodology

For each simulation:
1. The **yield** evolves over time by applying the expected growth rate plus a **random shock** (normally distributed with the configured volatility)
2. The **required capital** is calculated as: `capital = (monthly income × 12) / net yield`
3. After N simulations, the P5, P50 and P95 percentiles are extracted

---

## ⚠️ Disclaimer

This tool is for **illustrative and educational purposes only**. It does not constitute financial advice. Past performance does not guarantee future results.

---

## 📄 License

Distributed under the [MIT License](LICENSE).
