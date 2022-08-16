# Crypto Data Metric

## 1. Project Overview 
Combine all four layers of analytics (descriptive, diagnostic, predictive, and prescriptive) on crypto data in a dashboard format as a web application.

### 1.1. Problem Statement
A new FinTech company called Crypto Data Metric had a new product vision. They wanted to launch a subscription-based model, where they could sell analytics on crypto data to its customers.

As part of their offering, they were focused on Bitcoin and Ethereum. They want to combine different layers of analytics as a one-stop shop into a dashboard in a web application. This will help Crypto Data Metric’s customers answer their questions to make informed decisions.

1. Descriptive Analytics – What is the price of Bitcoin and Ethereum?

2. Diagnostic Analytics – Why is the price of Bitcoin and Ethereum going up or down? <br>
• Identify social, on-chain, and general statistical KPIs which affect the price. <br>
• Display the public’s sentiment on Bitcoin and Ethereum, which affect the price. <br>

3. Predictive Analytics – What will be the future price of Bitcoin and Ethereum?

4. Prescriptive Analytics – What decision should be taken knowing the future price of Bitcoin and Ethereum? <br>
• Trading Signal – Buy or Sell. <br>

5. Launch this product under the Crypto Data Metric domain. <br>
• Build the dashboard as a web application. <br>
• Link the web application to cryptodatametric.com. <br>

### 1.2. Solution
To bring Crypto Data Metric’s vision to life, the below steps are required.

1. Extract data from all different sources (websites & social media) using API and web scraping, transform and load it into a database. 

2. Move the data from the database to the data warehouse for machine learning and data analytics.

3. Machine learning <br>
• Understand public sentiment on Bitcoin and Ethereum (Diagnostic Analytics).
• Predict Bitcoin and Ethereum’s future prices (Predictive Analytics).
• Provide buy and sell signal (Prescriptive Analytics).

4. Data Analytics <br>
• Bitcoin and Ethereum’s latest prices (Descriptive Analytics). <br>
• Important KPIs that affect Bitcoin and Ethereum’s prices (Diagnostic Analytics). <br>

5. Display all the information in a dashboard as a web application with a domain link to Cryptodatametic.com.

6. Each step of the process should be automated.

### 1.3. Tools

Data Extraction - Python (Beautiful Soup, Request, Selenium, Pytrends, Praw, and Tweepy)

Data Storage <br>
• Python - Psycopg and SQL Alchemy <br>
• Postgres <br>

Data Orchestration - Windows Task Scheduler

Data Mining, Analysis, and Transformation - Python (Pandas, Numpy, Unicode Data, and Contractions)

Time Series Analysis, Text Mining, and NLP - Python (Sklearn, Feauture Engine, NLTK, Text Blob, Statsmodels, and Pmdarima)

Data Visualization <br>
• Python - Matplotlib and Seaborn <br>
• Power BI <br>

Web Application - Python (Streamlit)

Model Deployment <br> 
• Docker <br>
• AWS <br>

