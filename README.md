# Dividend-Calculator

## Description
A program that analyzes stock data to find stocks that have the highest dividend return from a set investment value. The program does this by reading a list of stocks and etfs with high dividend yield from a seperate text file. After this, the yahooFinance library is used to load desired stock data (stock symbol, yearly change, etc.) into a dictionary that is later formatted into a dataframe. Once in a dataframe, the data is cleaned by getting rid of stocks that have invalid values. A new column is then created by calculating dividends per share. Shares owned and quarterly dividend earnings are then calculated assuming an initial investment of 1000USD. Lastly, a scatterplot is derived from this data displaying these stocks on the axes of annual percent change and quarterly dividend earnings for the purpose of finding stocks with high growth and dividend return.

## Potential Calculation Errors and Problems Faced
While trying to request information using the yahooFinance python library, there were some problems loading the responses. The main issue when trying to load the responses was attempting to find yearly percent change. The causes associated with this problem were, stocks being too new, stocks not listed in yahooFinance, or stocks only listing year to date as an option. The effects of this problem were comparing ytd percent changes with trailing 12 month percent changes. When getting rid of stocks that had less than 15% growth it was possible that well/underperforming were incorrectly affected based on a "trailing 12 month percent change" criteria. This would mean that the only condition where the difference between ytd and the trailing 12 month is negligible is at the end of the calendar year.

## Resources Used
1. Stock List: https://www.tradingview.com/ 
2. Stock Data Library: https://pypi.org/project/yfinance/ 
3. Data Frame Library: https://pandas.pydata.org/ 
4. Data Ploting Library: https://matplotlib.org/
