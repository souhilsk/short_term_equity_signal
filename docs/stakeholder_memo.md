# Stakeholder Memo – Short-Term Equity Price Direction Prediction

## Audience
Proprietary Trading Desk – Quantitative Research & Execution Teams

## Problem Summary
We seek to develop a short-term trading signal capable of predicting intraday price direction for a basket of highly liquid equities. The model will be powered by limit order book features, volume imbalance, and short-term price momentum. Even marginal improvements in timing can deliver meaningful PnL uplifts in high-frequency environments where microstructure edge decays quickly.

## Why This Matters
Our trading desk’s current execution logic relies on static thresholds and simple momentum indicators. This approach leaves potential alpha untapped, especially in volatile conditions. A more dynamic, data-driven signal can help optimize entry/exit decisions and reduce slippage.

## Expected Outcome
A **predictive artifact** in the form of a Python-based signal-generation module, ready to integrate into the desk’s execution pipeline. The model’s quality will be evaluated with:
- Directional hit ratio (% of correct up/down predictions)
- Trading performance metrics (Sharpe ratio, PnL per trade, max drawdown)
- Latency compliance (<1 second from new tick to prediction)

## Assumptions & Risks
- Historical order book and trade data are available and reliable.
- Market microstructure relationships will remain stable enough for the model to generalize.
- Latency in production will match or improve upon research environment performance.
- Key risk: model overfitting to short-term historical patterns that may not persist.

## Next Steps
- Complete feature engineering and preliminary backtesting within the bootcamp timeframe.
- Deliver a backtest report with assumptions and risk disclosures.
- Provide integration guidelines for production deployment.
