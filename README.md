# Stateful-Long-Short-strategy
Long-Short strategy with tehnical indicators and take profit, stop loss and days counter exits
## How to Run the Strategy
### In an Online Environment

The strategy can be executed in an online environment using Jupiter or JupiterLab on the [Quantiacs personal dashboard](https://quantiacs.com/personalpage/homepage). To do this, clone the template in your
personal account.

### In a Local Environment

To run the strategy locally, you need to install the [Quantiacs Toolbox](https://github.com/quantiacs/toolbox).

## Strategy Overview

### Key Features:
-Universe: NASDAQ-100 stocks

-Trading Logic: Positions are created by calculated signals, with exits for take profit, stop loss, and day counting positions

-Indicators Used: Exponential Moving Average (EMA), True Range (TR), Average True Range (ATR), etc.

-State Management: Utilizes the Quantiacs state management system to maintain and update strategy state across different days.

## Strategy Overview

This strategy uses a stateful approach to manage long and short positions with exits.
It operates on NASDAQ-100 stocks and uses tehnical indicators to create trading signals.

### Strategy Components:
1. Data Loading and Preparation:
   Load stock data using qndata.stocks.load_ndx_data.
2. Strategy Function:
   Define the strategy function which computes the weights  based on entry and exit signals.
3. State Management:
   Use state to manage positions and exits dynamically.
   Due to the state requirement, this strategy and the exits only work with the multipass backtester
4. Backtesting:
   Use the multipass backtester to evaluate the strategy .
