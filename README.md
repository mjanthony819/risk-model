# Risk Model

Daily returns distribution and Value at Risk, estimated three ways, in the browser. Part of a set of
four quant projects; this one answers: how much can this portfolio lose on a bad day?

Live: https://mjanthony819.github.io/risk-model/

## What it does

- 12 years of real S&P 500 daily returns embedded; load your own Date,Close CSV for any series
- Returns histogram with a matched normal overlay, so the fat left tail is visible
- VaR at 95% and 99%, 1-day and 10-day horizons: historical, parametric (normal), and Monte Carlo (100k draws)
- Expected shortfall (average loss beyond VaR)
- Skewness and excess kurtosis, rolling 30-day annualised volatility, worst-10-days table
- Dollar losses scaled to a configurable portfolio value

## Stack

Single `index.html`. No frameworks, no build step, no API keys. Charts are hand-drawn on canvas.

## Honest note

The parametric number understates the tail (excess kurtosis on this window is about 14). The three
methods side by side make that concrete.

Built with AI assistance (Claude).
