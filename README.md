# stock-market-analysis
For a beginner retail investor, our project aims to simplify the investment & trading process by employing a more visually comprehensible medium. A plethora of strategies and techniques are currently used by the professional investors to predict the direction of a particular stock but none of those are made readily available to the retail investors. Our project performs a comparative analysis between different investment strategies for the end-users and provides them with a selection of potentially profitable stocks based on their inputs.
Dataset Pre-processing:
The historical data was extracted from QuantConnect, AlphaVantage, & ETF homepages. The obsolete columns were removed after which the data mainly comprised of Open, High, Low Close & Volume  (OHLCV) values corresponding to daily time-frame and was stored in normalized tables in the SQLite DB. The 5 aforementioned columns were then further used to generate other features - SMA (Simple Moving Average) and BB (Bollinger Band) known as Technical Indicators. 
 
 
 
Model Formulation:
The comparative analysis depends on the below five inputs that are provided by the end user:
1.	Name of the stock
2.	Capital amount
3.	Stop Loss / Risk appetite (% value relative to capital)
 
The inbuilt trading algorithm based on the positive & negative crossovers of 200 & 50 MA(Moving Averages) is then executed. The Buy/Sell signals are plotted against these crossovers using MatplotLib library to indicate to user the frequency of profitable as well as loss making trades in a given time duration. 
 

This visual representation is then made more concrete by crunching some stats while our model backtests the algorithm on the historical OHLC data available in the DB. A more statistically intensive result set is then displayed for the user for further diagnosis of their selected stock.
 
Conclusion and Way Forward
The analysis provided is still in a very nascent stage and can be accompanied by a further set of sophisticated approaches. 

•	One of them is the user-defined custom algorithm wherein our model provides the flexibility to configure various technical indicators and thus allowing the user to learn while experimenting with various set of technical indicators. 

• Another effective analytical approach could be by integrating the power of Machine Learning models such as regression and LSTM to compare the accuracy of our algorithm-based model and advising the most efficient trading algorithm to the user for a given stock.

References:

•	https://ntguardian.wordpress.com/2018/07/17/stock-data-analysis-python-v2/

•	https://github.com/RomelTorres/alpha_vantage
