# The Productivity Mirage: Why This Cycle Is Different

**A Systematic Macro Research Project**

This project demonstrates systemization of macro insights, independent thinking, and interdisciplinary analysis (economics + political economy + computer science).

## Thesis

The consensus view holds that AI will replicate the 1990s productivity boom — delivering low inflation, high growth, and sustained equity multiple expansion. This project challenges that assumption by demonstrating that the 1990s expansion was fundamentally enabled by *deflationary globalization* (cheap Chinese labor integration, falling goods prices, low energy costs), a structural tailwind that no longer exists. The current AI boom is occurring in an *inflationary multipolar world* characterized by onshoring, energy transition costs, fiscal dominance, and labor scarcity.

We build a systematic `ProductivityRegimeIndicator` that scores the macro environment on a continuous scale from -1 (deflationary productivity regime) to +1 (inflationary productivity regime), and show that equity multiples priced for a 1990s-style miracle are vulnerable to repricing.

## Structure

The analysis follows a Bridgewater Associates "Daily Observations" format:

1. **What Happened Then** — The structural drivers of the 1990s expansion
2. **What's Different Now** — Why the current macro environment is fundamentally unlike the 1990s
3. **How We Systematize This** — The `ProductivityRegimeIndicator` algorithm
4. **Market Implications** — Backtest results and forward-looking valuation stress test

## Data Sources

- **S&P 500** — via Yahoo Finance (`^GSPC`)
- **10-Year Treasury Yield** — via Yahoo Finance (`^TNX`)
- **US PCE Price Index** — via FRED (`PCEPI`)
- **US Unit Labor Costs** — via FRED (`ULCNBS`)
- **China PPI** — via FRED (`CHNCPIALLMINMEI` as proxy) or constructed proxy
- **Semiconductor Stocks** — via Yahoo Finance (SMH/NVDA as AI proxy)
- **Shiller CAPE Ratio** — via Robert Shiller's publicly available dataset

## Setup

```bash
pip install -r requirements.txt
```

You will need a free FRED API key from https://fred.stlouisfed.org/docs/api/api_key.html.

Set it as an environment variable before running:

```bash
export FRED_API_KEY="your_key_here"
```

Then open the notebook:

```bash
jupyter notebook productivity_mirage.ipynb
```

## Methodology Notes

- All data transformations are transparent and replicable
- The regime indicator uses z-score normalization to make cross-era comparisons valid
- The backtest applies a simple valuation adjustment — not a full trading strategy — to isolate the regime effect on equity pricing
- No look-ahead bias: all indicators use trailing data only

## Disciplines Drawn Upon

- **Economics**: Productivity measurement, Phillips Curve dynamics, real yield decomposition
- **Political Economy**: US-China decoupling, industrial policy (CHIPS Act, IRA), fiscal dominance
- **History**: Analogies to 1960s–70s regime shift (guns-and-butter → stagflation)
- **Computer Science**: Systematic indicator construction, signal processing, algorithmic backtesting

---

*Built for the Bridgewater Associates 2027 Investment Associate Intern application.*
