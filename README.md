# Pricing and Risk Sensitivities of Binary Options on Cryptocurrencies: A Case Study of Binance Coin (BNB-USD)
## Summary
This study investigates the pricing and risk characteristics of binary options written on Binance Coin (BNB-USD), a leading cryptocurrency. Using daily historical price data between June 24, 2021 and June 24, 2022, the project applies descriptive statistics, visualizations to explain the log returns and volatility of the market. The option pricing was carried out with three methods: the Binomial Tree model, Monte Carlo simulation, and the Black–Scholes formula. In addition, the analysis extends to option Greeks, providing insight into the sensitivities of option prices to market variables. Results confirm the highly volatile nature of cryptocurrency assets and the limitations of applying traditional pricing models without modification. The findings offer investors guidance on risk exposure and highlight the importance of advanced modeling approaches for crypto derivatives.

---
**Full Report**: See `BNB_Binary_Options_Report.pdf`

## Data Source
- Asset: Binance Coin (BNB-USD)
- Period: June 24, 2021 – June 24, 2022
- Spot price (S0): Closing price on June 23, 2022
- Source: Yahoo Finance
  
## Methodology

1. **Descriptive Analysis**: Computed daily and log returns, annualized volatility, and rolling volatility. Plotted price trends and return distributions.
2. **Option Pricing**: Binary cash-or-nothing put with strike K=$240 and maturity T=1 day priced using:
   - Black–Scholes closed-form solution
   - Monte Carlo simulation
   - Binomial Tree (CRR model)
3. **Greeks Analysis**: Delta, Gamma, Vega, Theta, Rho, and Speed computed to assess sensitivities.

## Results
- Descriptive statistics: Mean = $415.40, Std Dev = $98.60, Min = $197.04, Max = $654.32
- Annualized returns: Normal = 2.4%, Log = -29.9%
- Annualized volatility: ~80%
- Option prices (K=$240, T=1 day, S0 = close on June 23, 2022):
  - Binomial Tree: $0.8942
  - Monte Carlo: $0.8783
  - Black–Scholes: $0.8710
  - **Average: $0.8812**
- Greeks:
  - Delta = 0.0217
  - Gamma = -0.000127
  - Theta ≈ 41.98 annualized (0.115 per day)
  - Vega = -0.283
  - Rho = -0.016

## Discussion
- All three pricing models produced consistent results, averaging $0.88. 
- The Black–Scholes benchmark is efficient but limited by constant volatility assumptions.
- Monte Carlo simulation provided confidence intervals and flexibility.
- The Binomial Tree was useful but computationally intensive for large steps.
- Greeks show that **Theta (time decay)** and **Vega (volatility sensitivity)** dominate risks. Delta and Gamma were minimal at the chosen strike and maturity.

---
**Download Full Report**:  `BNB_Binary_Options_Report.pdf`

## Recommendations
- Binary options on BNB should be used tactically for short-term bets, not long-term hedges, due to rapid time decay.
- Volatility effects are unconventional (negative Vega), requiring careful interpretation.
- Investors should apply multiple pricing models and stress-test volatility to avoid overreliance on any single framework.


