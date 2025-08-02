# sentiment-model-quant

Sentiment-Driven Option Trading Dashboard 
An interactive Streamlit application that stimulates the impact of market sentiment on option pricing and profit/loss using the Black-Scholes model. The app allows users to visualise how changes in sentiment-driven volatility and price expectations affect option values and outcomes - backed by a persistent relational database that maps each simulation's inputs and outputs for analysis and future learning. 

Features: 
	Sentiment integration: input a stock ticker, receive a recent/ real time sentiment score
 	Map sentiment score to expected stock volatility and price change assumptions 
	Options Pricing Engine: Black Scholes calculator for call and put options. Compute P/L based on user-defined purchase prices and simulate scenarios across a grid of volatility and price shocks 
 Heatmap visualisation: Interactive heatmap displays P/L outcomes based on sentiment-driven volatility and price changes, where green = positive P/L and red = negative P/L
 Database integration: Save all the simulations to a relational database. The inputs and outputs are stored in separate, linked tables: 
 - Inputs table: ticker, date, sentiment score, base volatility, user prices
 - Outputs table: volatility and price shocks, calculated P/L, calculation ID
	Modular UI via Streamlit: Intuitive controls for selecting ticker, sentiment scenario and purchase price + tabs for simulation, history and summary stats

Notebooks directory: 
notebooks/ contains experimental and research driven components of the project, which are used to prototype the models and logic before productionising them in src/

| Notebook                      | Purpose                                                                                                                      
| `1_data_exploration.ipynb`    | Loads historical stock data and explores pricing, volume, volatility patterns                                                    |
| `2_sentiment_modeling.ipynb`  | Scrapes headlines or social media content, scores sentiment using VADER / finBERT, and analyzes correlation with market movement |
| `3_feature_engineering.ipynb` | Engineers features such as sentiment rolling average, volatility bands, or lagged returns for model input                        |
| `4_backtesting.ipynb`         | Simulates trading strategies using sentiment-influenced option pricing; validates P/L predictions vs historical movements    
 	
