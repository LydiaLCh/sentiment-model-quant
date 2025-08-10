# Section Title: Data Exploration

## 1. Purpose
Understand the dataset: the structure, quality and the relationships inside of it. This will ensure that there is a clean input and reliable outputs from the option pricing simulations. 
## 2. Key Concepts

Goals: 
* Dataset Documentation:
	* Interpreting the data: meaning of each column in the dataset, expected ranges / units for output variables such as sentiment score, volatility and prices, imputing data and check for correct formatting of dates / consideration of timezones, etc. 
	* Categorising data: numerical, time-series, textual (raw tweets encoded into sentiment scores) , categorical 
* Exploratory Data Analysis: 
	* Univariate Analysis: visualise distributions by plotting histograms / density plots of sentiment scores to see if the sentiment is mostly neutral, +ve / -ve, plot box plots for volatility and P/L to identify typical ranges and outliers
		* Concepts to study: skewness / kurtosis, outlier detection, log returns 
	* Missing value Analysis: Visualise missingness pattern with heatmaps, imputation (interpolation or forward fill) vs dropping 
	* Bivariate & Multivariate Relationships: 
		* Correlation matrices using Pearson / Spearman (rank-based correlation) between input variables and output 
		* Scatter plots: for correlation visualisation 
		* Heatmaps to visualise the correlation matrices 
		* Pairplots: examine joint distributions and potential non-linear relationships 
	* Time Series inspection
		* Visualise trends 
		* Resample / aggregation of data weekly or monthly to sooth noise and observe long term trends 
		* Stationarity: use rolling mean plots
	* Domain-specific metrics (Finance)
		* Price returns 
			* Log returns 
			* Realised volatility 
		* Options Metrics 
			* Strike price, expiry, implied volatility 
			* Price skew/ distribution of strikes
* Understanding Sentiment data 
	* Volume of tweets / day: data density & reliability 
	* Distribution of sentiment scores: cluster / variation 
	* Lagged effects: cross-correlations with lag shifts to determine if current sentiment affects future volatility 
* Data cleaning and Preprocessing techniques 
	* Datatime parsing / alignment: alignment of sentiment timestamps with market data timestamps to handle time shifts / missing data
	* Normalisation / standardisation
	* Duplicates: detect / drop duplicate rows
	* Handle specific cases such as non-trading days using forward fill to maintain alignment 
* Tools and Libraries to use: 
	* pandas, numpy 
	* matplotlib, seaborn 
	* scipy.stats 
	* statsmodels 
	* missing or ydata-profiling 

## 3. Insights / Conclusions 

Features in a [[historical price dataset]]  
In markets overnight, when exchanges are closed, market-moving information still flows in [[markets overnight]] 

Conclusions: 
1. Sampling frequency chosen: 
	Hourly frequency to align with sentiment scores: captures intraday movement and align with multiple sentiment updates, while not being overly noisy and dominated by bid/ask jumps or low liquidity, and being a manageable data size. Additionally, with hourly data, I can resample it to daily/weekly if needed, but still zoom in on intraday sentiment-to-price impact. 
2. [[Missing Value analysis]]
3. [[concepts/IQR vs MEDIAN]] 
4. [[concepts/Pearson correlation]] 
5. [[concepts/Spearman correlation]]
6. [[concepts/Sentiment Analysis]] 
7. 


## 4. Links / References
- External reading (Investopedia, papers, docs)
- Notes for revisiting

## 5. TODO / Revisit
- Gaps in understanding
- Questions to explore in later sections