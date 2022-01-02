# Stock-Market-Forecasting-Analysis
![Project banner](https://github.com/Sid-075/Stock-Market-Forecasting-Analysis/blob/main/images/banner.jpg)
## About
Stock Market Forecasting & Analysis is a project that uses time series analysis to show seasonal patterns and trends. I used time series values for forecasting most profitable stocks of 2019.

'*All_stocks_2010-2018*' is the dataset based on which the project has been built. The csv file can be found in the 'Dataset' directory of this repository.

My analysis is twofold:
	1.	To predict 2019 values and compare it with the existing data (2019).
	2.	To predict the most profitable stocks of 2019 using Clustering models.

The time series analysis was split into 4 parts:
	-	Level: The base value for the series if it were a straight line.
	-	Trend: The linear increasing or decreasing behavior of the series over time.
	-	Seasonality: The repeating patterns or cycles of behavior over time.
	-	Noise: The variability in the observations that cannot be explained by the model.

The dataset contains data from 2010-2019 retrieved from Yahoo finance using a library called pandas data reader. The time series model is used to predict the 2019 stock data by comparing it to the existing data. For the time series model, the opening price of every stock is taken as most important variable for prediction of 2019 data.

I used 2 models, SARIMA and Facebook Prophet model.
 
Facebook Prophet model was used as it can fit nonlinear trends with yearly, weekly and daily seasonality. SARIMA model takes into account, seasonality, trend, and noise in the data. The seasonal parameter is set at 12 (monthly data).

*To predict 2019 values and compare it with the existing data (2019)*

To evaluate the models performance, I calculated the mean square error of my dataset to test the authenticity of the model. For instance, the mean squared error of SARIMA model for the stock Microsoft was 0.191 compared to mean squared error of Facebook Prophet model was 2.915. The MSE of SARIMA for Microsoft was low enough to be confident about the model’s ability to predict accurately in the future. Hence SARIMA turned out to be a better model than Facebook Prophet model.

*To predict the most profitable stocks of 2019 using Clustering models*

Developed clustering on the given data from 2010-2018 based on the attribute annual returns to find out the top 4 profitable stocks in the market in the given period. I used K means clustering with 10 iterations, Agglomerative clustering with single linkage method and complete linkage method and DB Scan. I evaluated the clustering models using Silhouette coefficient where K means clustering turned out to be the best model with the Silhouette coefficient of 0.55.

The most profitable stocks were Disney, AT&T, Microsoft, Kraft & Heinz.

## How to run this project?
*Note: This project is run on Anaconda distribution.*
	1. Clone the repositiory into your workspace using the code link.
	2. Install pip version 2.19.1.1 through command pip install pystan==2.19.1.1
	3. Install the required libraries using the command pip install requirements.txt
	4. Open IPython Notebook: 2019StockMarketAnalysis.ipynb with Jupyter Notebook.
	5. Run the Notebook to view the results.

## Data Visulizations

