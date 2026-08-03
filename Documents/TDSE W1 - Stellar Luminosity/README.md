# Stellar Luminosity — Linear and Polynomial Regression from First Principles
 
Author - Julian Santiago Ramirez Urueña.

This project implements vectorized linear and polynomial regression from
scratch (no ML libraries) to model the relationship between stellar mass
and luminosity, in order to understand how a regression model learns from
data at the level of representation, prediction, error, and gradient-based
optimization.
 
## Requirements
 
- Python 3
- NumPy
- Matplotlib

## How to Run
 
1. Clone this repository.
2. Install the dependencies: `pip install numpy matplotlib`.
3. Open `stellar_luminosity_hands_on.ipynb` in Jupyter and click on "run all".

## Main Result
 
A single-feature linear model underfits the data (final cost ≈ 9.80),
systematically missing the curvature of the mass-luminosity relation. Reusing
the exact same prediction, cost, and gradient-descent functions on a
polynomial representation (`mass`, `mass²`) drops the final cost to ≈ 0.32
and removes the systematic error pattern — the same learning algorithm
performs very differently depending only on how the input is represented.
Extrapolating either model far outside the observed mass range (0.6-2.4
solar masses) is not supported by the data, regardless of which prediction
looks more plausible.