# Capital Asset Pricing Model (CAPM)

This repository contains a Python implementation of the Capital Asset Pricing Model (CAPM) using historical market data. The project demonstrates how to calculate daily returns, estimate beta and alpha through linear regression, and visualize the relationship between a stock and the market.

## Overview

The notebook walks through the following steps:

- Importing and cleaning historical stock and index data
- Calculating daily returns
- Performing a CAPM regression using `numpy.polyfit`
- Estimating beta (market sensitivity) and alpha (excess return)
- Creating visualizations with Plotly
- Interpreting the results

The main file in this repository is:

`Capital_Asset_Pricing_Model_(CAPM).ipynb`

## Technologies Used

- Python 3
- Pandas
- NumPy
- Plotly Express
- Matplotlib
- Jupyter Notebook

## Key Concepts

### Daily Returns

```
df['return'] = df['Close'].pct_change()
```

### Beta and Alpha Estimation

```
beta, alpha = np.polyfit(market_returns, stock_returns, 1)
```

### Interpretation

- Beta > 1: stock is more volatile than the market
- Beta < 1: stock is less volatile
- Alpha: return independent of market movements

## Visualizations

The notebook includes:

- Stock price trend
- Scatter plot of stock vs. market returns
- CAPM regression line
- Return distributions

### Example

```
fig = px.line(df, x='Date', y='Close', title='Stock Price Over Time')
fig.show()
```

## Project Structure

```
CAPM-Project/
│
├── Capital_Asset_Pricing_Model(CAPM).ipynb
└── README.md
```

## How to Run

1. Clone the repository:

```
git clone <your-repo-url>
```

2. Install requirements:

```
pip install pandas numpy plotly matplotlib
```

3. Launch the notebook:

```
jupyter notebook
```

4. Run all cells in order.

## License

This project is released under the MIT License.

## Contributions

Contributions are welcome. Feel free to submit pull requests or open issues for suggestions.
