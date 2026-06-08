# QuantaFlex ETF

QuantaFlex ETF is a proposed **rules-based, actively managed multi-asset ETF** designed to allocate across equities, fixed income, commodities, and cash using transparent quantitative methods. This repository contains the full term project, including Checkpoints A, B, and C, the final written prospectus, code, figures, tables, and supporting outputs.

## Project Summary

The goal of QuantaFlex ETF is to combine:

- diversified multi-asset exposure,
- transparent rules-based portfolio construction,
- basic risk management,
- and quantitative evaluation using historical data and Monte Carlo simulation.

The project begins with a baseline long-only equal-weight portfolio and evaluates whether this approach could serve as the foundation for a future actively managed ETF.

## Asset Universe

The initial portfolio includes:

- **NVDA** - U.S. growth equity
- **AGG** - U.S. investment-grade bonds
- **ACWI** - global equities
- **GLD** - gold
- **DBC** - broad commodities
- **BIL** - cash / Treasury-bill reserve

Benchmark:

- **SPY** - S&P 500 ETF

## Key Findings

The baseline QuantaFlex portfolio produced these approximate historical results over 2008–2024:

| Metric | QuantaFlex | SPY |
|---|---:|---:|
| Annualized Return (%) | 8.03 | 10.85 |
| Annualized Volatility (%) | 12.92 | 19.95 |
| Sharpe Ratio | 0.62 | 0.54 |
| Maximum Drawdown (%) | -39.54 | -51.48 |
| Alpha (%) | 2.64 | — |
| Beta | 0.50 | — |

Monte Carlo testing also suggested positive expected growth:

- **Mean 5-year ending value**: ~1.55
- **Median 5-year ending value**: ~1.50

## Repository Structure

**`checkpoints/`**
- `checkpoint_a.md`
- `checkpoint_b.md`
- `checkpoint_c.md`

**`final_report/`**
- `final_term_project.md`
- `final_term_project.pdf`

**`notebooks/`**
- `Checkpoint_B_Notebook.ipynb`
- `Checkpoint_C_Notebook.ipynb`

**`data/`**
- `quantaflex_prices.csv`
- `quantaflex_log_returns.csv`
- `quantaflex_summary_stats.csv`
- `quantaflex_portfolio_metrics.csv`
- `quantaflex_c_fee_analysis.csv`
- `quantaflex_c_scenario_summary.csv`

**`figures/`**
- `normalized_prices.png`
- `buy_and_hold_vs_spy.png`
- `monte_carlo_histogram.png`

**`presentation/`**
- `QuantaFlex_Presentation.pdf`
- `presentation_script.md`

## How to Run

### Requirements

Install:

```bash
pip install numpy pandas matplotlib yfinance
```

### Run notebooks

Open and run:

- `notebooks/Checkpoint_B_Notebook.ipynb`
- `notebooks/Checkpoint_C_Notebook.ipynb`

These notebooks:

- download and clean market data,
- compute daily log returns,
- build the baseline portfolio,
- compare results to SPY,
- calculate performance metrics,
- and run Monte Carlo simulation.

## Final Recommendation

QuantaFlex ETF appears promising as a **research-driven, lower-risk multi-asset strategy**, but not yet strong enough in its baseline form to justify launching a firm immediately. The next stage would be to test the active trading rules and determine whether the strategy can produce enough post-fee alpha to support a viable business.

## GenAI Tools

Generative AI tools were used to assist with:

- brainstorming project structure,
- improving report wording,
- organizing GitHub documentation,
- and refining code explanations.

All final analysis, results, code execution, and submission materials were reviewed and edited by the student before submission. Conversation logs or summaries can be added to the repository if required by the instructor.
