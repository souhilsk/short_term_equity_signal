# Short-Term Equity Signal
Short-Term Equity Price Direction Prediction

**Stage:** Problem Framing & Scoping (Stage 01)  

## Problem Statement  
This project aims to design and evaluate a short-term trading signal that predicts intraday price direction for a basket of highly liquid equities. The model will leverage limit order book features, volume imbalance, and recent price momentum as predictive inputs. The problem is important because even small improvements in entry and exit timing can have a material impact on profitability for high-frequency strategies, especially in competitive markets where microstructure edge decays quickly.

## Stakeholder & User  
The primary stakeholder is a proprietary trading desk operating intraday equity strategies. Quantitative researchers will design and validate the model, while traders or automated execution systems will consume the output in real time. The signal needs to integrate into an existing execution pipeline with minimal latency, and decisions must be made within milliseconds to seconds of new data arrival.

## Useful Answer & Decision  
The desired answer is predictive, a statistical model producing a binary or probabilistic forecast of the next price move direction (up/down). The core evaluation metric will be directional hit ratio, complemented by trading-specific measures such as realized PnL per trade, Sharpe ratio, and drawdown. The deliverable will be an artifact: a deployable Python module that generates signals, accompanied by a backtest report detailing performance, assumptions, and risk factors.

## Assumptions & Constraints  
- **Data Availability:** Historical limit order book data and trade data for selected equities is accessible via an API or local datasets.  
- **Latency Requirements:** Predictions must be generated within sub-second timeframes to be usable in production.  
- **Feature Stability:** Predictive features remain relevant and are not quickly arbitraged away during the testing period.  
- **Regulatory Compliance:** Strategy operates within market regulations (e.g., avoiding spoofing or manipulative practices).  

## Known Unknowns / Risks  
- Potential overfitting due to the high dimensionality of microstructure data.  
- Signal degradation if market microstructure dynamics change significantly.  
- Latency bottlenecks when moving from research to production environment.  
- Data quality issues (e.g., missing ticks, out-of-order updates) impacting model accuracy.  

## Lifecycle Mapping  
Goal → Stage → Deliverable  
- Identify features predictive of short-term price direction → Data Acquisition & Preprocessing → Feature dataset  
- Develop and evaluate classification model → Modeling & Evaluation → Backtest performance report  
- Prepare real-time signal module → Results Reporting & Delivery Design → Deployable Python artifact  

## Repo Plan  
- `/data/` → Raw and processed datasets (excluded from repo if proprietary)  
- `/src/` → Python modules for feature engineering, modeling, and evaluation  
- `/notebooks/` → Jupyter notebooks for exploration, EDA, and prototyping  
- `/docs/` → Stakeholder memo, model documentation, and presentation slides  

Cadence: Update notebooks and src as milestones are completed; commit regularly after significant changes.
