# NSE Stock Portfolio Optimization

A Shiny dashboard application that helps investors optimize their portfolio allocation across NSE (National Stock Exchange of India) top 100 stocks based on different investment objectives. The app uses Modern Portfolio Theory to calculate optimal portfolio weights and visualize the efficient frontier.

## Features

- Select multiple stocks from NSE Top 100 companies
- Choose from three investment objectives:
  - Maximize Returns
  - Minimize Risk
  - Maximize Sharpe Ratio
- Adjustable risk-free rate
- Custom investment amount input
- Interactive visualization of the efficient frontier
- Detailed allocation weights and amounts for each stock

## Prerequisites

- R version 4.0.0 or higher
- Required R packages:
  ```R
  install.packages(c(
    "shiny",
    "shinydashboard",
    "quantmod",
    "PerformanceAnalytics",
    "fPortfolio",
    "timeSeries",
    "dplyr"
  ))
  ```

## Installation

1. Clone this repository
```bash
git clone https://github.com/yourusername/nse-portfolio-optimization
cd nse-portfolio-optimization
```

2. Run the Shiny application
```R
source("app.R")
```

## Usage

1. Select two or more stocks from the dropdown menu
2. Choose your investment objective:
   - Maximize Returns: Focuses on highest potential returns
   - Minimize Risk: Creates the lowest volatility portfolio
   - Maximize Sharpe Ratio: Maximizes return per additional unit of risk taken
3. Adjust the risk-free rate (default: 7%)
4. Enter your total investment amount in Indian Rupees
5. Click "Calculate amounts to be allocated"
6. View the results in the "Results" tab:
   - Portfolio weights table
   - Efficient frontier visualization

## Data Source

The application fetches stock data from Yahoo Finance using the following parameters:
- Time period: 2021-07-31 to 2024-07-31
- Data type: Adjusted daily closing prices
- Market: NSE (National Stock Exchange of India)

### Portfolio Optimization Functions

- `getSymbols()`: Fetches stock data from Yahoo Finance
- `Return.calculate()`: Calculates returns from price data
- `minvariancePortfolio()`: Calculates minimum variance portfolio weights
- `tangencyPortfolio()`: Calculates maximum Sharpe ratio portfolio weights
- `portfolioFrontier()`: Generates efficient frontier data

## Limitations

- The application uses historical data for optimization, which may not predict future performance
- Transaction costs and taxes are not considered in the optimization
- Only supports long-only portfolios (no short selling)
- Limited to NSE Top 100 stocks

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

- Data provided by Yahoo Finance
- Built using the R Shiny framework
- Portfolio optimization calculations based on Modern Portfolio Theory

## Contact

Kolla Vinay Sai - mail to : kollavinaysai@gmail.com

Project Link: [https://github.com/yourusername/nse-portfolio-optimization](https://github.com/yourusername/nse-portfolio-optimization)
