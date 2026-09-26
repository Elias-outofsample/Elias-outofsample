## Quantitative research · data engineering · evaluation

I build research tooling where a result has to survive scrutiny before anyone relies on it:
data served as it was known at the time, backtests judged by statistics rather than by their
best Sharpe ratio, and retrieval systems in which every design choice is measured.

### Projects

**[rigor](https://github.com/Elias-outofsample/rigor)** — a reproducible research framework for
systematic trading strategies. Twelve statistical gates (deflated Sharpe ratio, probability
of backtest overfitting, the t > 3 hurdle, walk-forward efficiency, bootstrap intervals, …)
turn a backtest into a verdict: PROMOTE, CONDITIONAL or REJECT. Sixteen example strategies
with their research theses; CI recomputes every published number.
`Python · pandas · NumPy / SciPy · FastAPI · mypy · 1,111 tests`

**[spx-options-pipeline](https://github.com/Elias-outofsample/spx-options-pipeline)** — a
point-in-time data lake for SPX options research. One-minute Greeks, quotes, implied
volatility surfaces, open interest and trades in a partitioned Parquet store, served through
DuckDB with look-ahead guards: as-of cutoffs, regime lags, per-contract feature lags. Ships a
synthetic data generator, so it runs without a data subscription.
`Parquet · DuckDB · Polars · Arrow · 107 tests`

**[quant-rag](https://github.com/Elias-outofsample/quant-rag)** — retrieval over a library of
quantitative-finance research, served to LLM agents. Leak-controlled benchmarks, paired
bootstrap confidence intervals and placebo arms settled every design choice, and rejected
most of the popular ones. Passages arrive whole with a verifiable anchor; quotes are checked
without a language model.
`Qdrant · Qwen3 embeddings · Model Context Protocol · 546 tests`

### How I work

- A difference without its confidence interval, or without a placebo run beside it, is not
  a result.
- Data is served as it was known at the time, or not at all.
- A number quoted in a README is recomputed in CI.
- Negative results are kept and written down.

### Toolbox

Python (pandas, Polars, NumPy, SciPy) · SQL and DuckDB · Parquet and Arrow · statistics of
backtest validation · FastAPI · pytest and Hypothesis · mypy · GitHub Actions · Qdrant ·
PyTorch (inference)
