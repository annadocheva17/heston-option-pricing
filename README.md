# Heston Option Pricing and Calibration

Anna Docheva and Julien Kanaan

This notebook simulates the Heston stochastic volatility model, estimates European call prices by Monte Carlo, and trains a PyTorch neural network to approximate those prices. It calibrates the surrogate to AAPL call quotes, examines the effects of restricted moneyness and maturity in the training data, and compares the baseline with a revised surrogate and an implied-volatility smile.

## Run the notebook

1. Install the dependencies with `python -m pip install -r requirements.txt`.
2. Open `heston_option_pricing.ipynb` from the repository root in Jupyter and run the cells in order. The simulation and training generate the synthetic prices, checkpoint, and scalers.
3. To run market calibration and the smile comparison, place `AAPL_Call.csv` beside the notebook. The loader expects semicolon-separated columns named `Strike`, `Bid`, and `Ask`. The original analysis uses quotes dated December 26, 2025, with expiry December 18, 2026. For a different snapshot, update the spot price, rate, and dates in the calibration section.

The notebook includes saved figures and summary results. The original AAPL quote file is required to reproduce the market calibration.
