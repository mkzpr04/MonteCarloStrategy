## Monte Carlo Arbitrage Strategy on Polymarket

Ethereum above $2,700 on February 21?

# Overview

Arbitrage Detection through Monte Carlo Simulation to assess if a rating is undervalued or overvalued on polymarket

# Methodology

1. Data Processing & Return Adjustments

- The mean of daily returns is removed to focus purely on volatility, as market drifts can introduce biases in short-term predictions.
- We apply exponential weighting to give more importance to recent data, capturing the volatility dynamics in crypto markets.

2. Monte Carlo Simulations
- We simulate thousands of price paths assuming returns follow a normal distribution 
Volatility is estimated from historical returns and dynamically adjusted using exponential weighting to adapt to recent market conditions.

3. Probability Estimation & Arbitrage Detection
- We compute the fraction of simulated paths that exceed the target price at the given date.
- The probability can be converted into betting odds and compared to Polymarket’s odds.
- If our model's implied probability differs significantly from Polymarket’s, an arbitrage opportunity is identified.

# Example Case
For ETH > $2700 on Feb 21:

Our model estimates a 57.62% probability, while Polymarket prices it at 59%.

If:
Polymarket YES odds: 1.45 (1/0.69)
Model YES odds: 1.72 (1/0.58)
Then the difference is large enough, so it signals a potential arbitrage trade.


# Next steps
- Integrate an AI-based decision layer to refine arbitrage opportunities.
- Enhance the model
- Refine stochastic modeling: Incorporate factors like volatility clustering or regime shifts.
- Special project that I would love to developp: Automate arbitrage detection: Develop a bot to scan and execute trades when discrepancies arise and combine this with a scrapping algorithm.
- Expand to other markets: Apply the same approach to different assets and prediction platforms
