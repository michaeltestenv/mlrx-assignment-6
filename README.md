# Linear Regression Experiments

This project is an interactive web app for experimenting with a simple linear regression setup and repeated simulation.

## What it does

The app lets the user choose parameters such as:

- sample size `N`
- noise mean `mu`
- noise variance `sigma^2`
- number of simulations `S`

It then:

1. generates a random dataset
2. fits a linear regression model
3. plots the fitted regression line
4. runs repeated simulations
5. shows histograms of estimated slopes and intercepts
6. reports how often simulated values are more extreme than the initially observed fit

## Main features

- Flask-based web interface
- Regression line plot
- Histogram visualization for repeated simulations
- Simple demonstration of sampling variability in linear regression

## Repository contents

- `app.py` - Flask app and simulation logic
- `templates/index.html` - Input form and output page
- `requirements.txt` - Python dependencies

## How it works

The code generates random `X` values, creates `Y` using normal noise, fits a `LinearRegression` model from scikit-learn, and repeats that process many times to visualize the distribution of fitted coefficients.

This makes the project useful as a teaching or intuition-building tool for:

- linear regression
- coefficient variability
- repeated simulation / Monte Carlo-style reasoning

## Run locally

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Start the app:
   ```bash
   python app.py
   ```
3. Open the local Flask page in your browser and enter values for `N`, `mu`, `sigma^2`, and `S`.

## Why this repo is useful

This repo is a compact demonstration of how to turn a basic statistics / regression assignment into an interactive app instead of a static notebook.
