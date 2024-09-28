# Prime-AI

This project analyzes historical trade data from various Binance accounts over a 90-day period. It calculates several financial metrics such as ROI, PnL, Sharpe Ratio, Maximum Drawdown (MDD), Win Rate, and others to rank the accounts based on their performance.
Dataset Description
The dataset contains the following key information:

Port_IDs: Unique identifier for each Binance account.
Trade_History: Historical trades in a JSON-like string format, containing details such as:
time: Timestamp of the trade.
symbol: The asset being traded.
side: Whether it was a BUY or SELL trade.
price: The price of the asset at the time of the trade.
fee: Transaction fee.
quantity: Amount of money involved in the trade.
realizedProfit: The profit or loss made in the trade.

Objectives
Analyze the Dataset: Clean, explore, and parse the dataset.
Feature Engineering: Extract necessary features from Trade_History to calculate financial metrics.
Ranking Algorithm: Rank the accounts based on multiple financial metrics to determine the top-performing accounts.
Provide a Report: Summarize methodology, findings, and assumptions.

Metrics Calculated
For each account, the following financial metrics are calculated:

ROI (Return on Investment): Measures the profitability of an account's trades relative to the investment.
PnL (Profit and Loss): Total profit or loss made by the account.
Sharpe Ratio: Measures the risk-adjusted returns of the account.
MDD (Maximum Drawdown): The largest peak-to-trough decline observed in the account's cumulative returns.
Win Rate: Percentage of trades that resulted in a profit.
Win Positions: Number of profitable positions.
Total Positions: Total number of positions taken by the account.
Ranking Methodology
The accounts are ranked based on a weighted scoring system that combines the following metrics:

ROI: Higher ROI contributes to a better rank.
PnL: Higher profit leads to a better rank.
Sharpe Ratio: Accounts with better risk-adjusted returns are ranked higher.
MDD: Lower MDD leads to a better rank.
The final rank is computed by combining the ranks of these metrics. The accounts with the lowest overall rank are the top performers.

Results
The results will be saved in top_20_accounts.csv, containing the following columns:

Port_ID: The account identifier.
ROI: The return on investment.
PnL: The profit and loss.
WinRate: The win rate of the account.
WinPositions: The number of profitable trades.
TotalPositions: The total number of trades.
SharpeRatio: The Sharpe Ratio of the account.
MDD: The maximum drawdown.
Rank: The overall rank of the account.
