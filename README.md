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

### 1.4. Technical Skills
Data Analysis <br>
Data Mining <br>
Data Orchestration <br>
Data Visualization <br>
Data Transformation <br>
ML Deployment <br>
Web Application <br>
Data Storytelling <br>
NLP & Text Mining <br>
Time Series Forecasting <br>
ETL <br>
Database Design <br>
Data Warehouse Design <br>
Web Scraping <br>
Programming (SQL and Python) <br>

### 1.5. End to End Process Flowchart
![image](https://user-images.githubusercontent.com/99619460/184965051-de786019-b4db-47d3-9a4a-29891e86895a.png)

### 1.6. Data Source
#### 1.6.1. Structured Data - API
![image](https://user-images.githubusercontent.com/99619460/184965276-d84cdc43-f01d-44d9-8a25-56c7f536ec0e.png)

#### 1.6.2. Structured Data - Web Scraping
![image](https://user-images.githubusercontent.com/99619460/184965368-08fd42d5-94dd-4d33-bb38-384111d8f5db.png)

#### 1.6.3. Unstructured Data - API
![image](https://user-images.githubusercontent.com/99619460/184965456-ed12fd6f-4eb6-486b-895a-006832f2f678.png)

## 2. Data Engineering Pipeline
The below visual explains the data engineering pipeline required to build the product.

![image](https://user-images.githubusercontent.com/99619460/184965611-65984931-800b-44a8-8f74-f366258cfbfd.png)

### 2.1. ETL Pipeline

The ETL pipeline is a set of processes used to move data from one source or multiple sources into a database. The three interdependent steps include extraction, transformation, and loading so that data can be integrated from various sources and stored in one centralized source (database).

#### 2.1.1. Structured Data

All structured data is extracted via API and web scraping.

Below is the flowchart of the process.

![image](https://user-images.githubusercontent.com/99619460/184965772-f7d86c0d-b7b5-4f2e-934c-8ae2fe1ec25b.png)

#### 2.1.1.1. API
Data is extracted via API, transformed using Python, and loaded into Postgres Database. All the Python scripts are automatically running at set intervals using the windows task scheduler.

Below is a flowchart of the process.

![image](https://user-images.githubusercontent.com/99619460/184965926-67ba91e6-94f2-41ca-81fb-3e829f9d6cbb.png)

Three different Python scripts are running to extract data via API. Below is the list of files. <br>
Ø Bitcoin On-chain Analytics <br>
Ø Ethereum On-chain Analytics <br>
Ø Bitcoin & Ethereum General Stats <br>

The below section explains each Python script and code linked to the script.

##### 2.1.1.1.1. Bitcoin On-chain Analytics

This script is extracting Bitcoin’s On-chain analytics data from Glassnode.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/bitcoin_on-chain_analytics

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

##### 2.1.1.1.2. Ethereum On-chain Analytics

This script is extracting Ethereum’s On-chain analytics data from Glassnode.com via API. Python transforms that data and loads it into the Postgres database

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/ethereum_on-chain_analytics

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

##### 2.1.1.1.3. Bitcoin & Ethereum General Stats

This script extracts Bitcoin and Ethereum’s general data from Coinmarketcap.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/bitcoin_%26_ethereum_general_stats

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

#### 2.1.1.2. Web Scraping

Data is extracted via web scraping, transformed using Python, and loaded into Postgres Database. All the Python scripts are automatically running at set intervals using the windows task scheduler.

Below is a flowchart of the process.

![image](https://user-images.githubusercontent.com/99619460/184968459-2fc81a1a-793c-4495-897e-eb744aae75ea.png)

Five different Python scripts are running to extract data via web scraping. Below is the list of files. <br>
Ø Altcoin Index Stats <br>
Ø Bitcoin & Ethereum Social Stats <br>
Ø Bitcoin Network Stats <br>
Ø Bitcoin Historical Prices <br>
Ø Institutional Holdings <br>

The below section explains each Python script and code linked to the script.

##### 2.1.1.2.1. Altcoin Index Stats

This script extracts Bitcoin’s performance data compared to altcoins from Blockchaincenter.net via web scraping. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/altcoin_index_stats

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

##### 2.1.1.2.2. Bitcoin & Ethereum Social Stats

This script extracts Bitcoin and Ethereum’s social data from Bitinfocharts.com via web scraping. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/bitcoin_%26_ethereum_social_stats

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

##### 2.1.1.2.3. Bitcoin Network Stats

This script extracts Bitcoin on-chain analytics data from Coin.dance via web scraping. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/bitcoin_network_stats

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

##### 2.1.1.2.4. Bitcoin Network Stats

This script extracts Bitcoin historical price data from Coin.dance via web scraping. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/bitcoin_historical_prices

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

##### 2.1.1.2.5. Institutional Holdings

This script extracts Bitcoin & Ethereum’s institutional data from Tokenview.com via web scraping. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/institutional_holdings

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

#### 2.1.2. Unstructured Data
All unstructured data is extracted via API.

Below is the flowchart of the process.

![image](https://user-images.githubusercontent.com/99619460/184971793-d82c90cc-7a13-475f-b7df-69740541b64c.png)

##### 2.1.2.1. API

Data is extracted via API, transformed using Python, and loaded into Postgres Database. All the Python scripts are automatically running at set intervals using the windows task scheduler.

Below is a flowchart of the process.

![image](https://user-images.githubusercontent.com/99619460/184971860-2ceaf62b-2cf9-4e54-b5d9-3b1ef8e50669.png)

Six different Python scripts are running to extract data via API. Below is the list of files. <br>
Ø Reddit Post  <br>
Ø Reddit Comments <br>
Ø Google Trend <br>
Ø Crypto News <br>
Ø Twitter Keyword <br>
Ø Twitter User <br>

The below section explains each Python script and code linked to the script.

###### 2.1.2.1.1. Reddit Post

This script is extracting Reddit posts from Reddit.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/reddit_post

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

###### 2.1.2.1.2. Reddit Comments

This script is extracting Reddit comments from Reddit.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/reddit_comments

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

###### 2.1.2.1.3. Google Trend

This script extracts the Google Trend score from Trends.google.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/google_trend

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

###### 2.1.2.1.4. Crypto News

This script extracts Crypto news from Crypto.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/crypto_news

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

###### 2.1.2.1.5. Twitter Keyword
This script extracts Tweets based on keywords from Twitter.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/twitter_keyword

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

###### 2.1.2.1.6. Twitter User
This script extracts Tweets based on real-time user data from Twitter.com via API. Python transforms that data and loads it into the Postgres database.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/twitter_user

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

### 2.2. Database Design

Database design is a crucial aspect data lifecycle process. Data collected via API and web scraping must be stored in a database for data analytics and machine learning. 

#### 2.2.1. Structured Data
##### 2.2.1.1. Table & Flowchart

Data is extracted via API & web scraping, transformed, and loaded into the below tables in Postgres Database.

![image](https://user-images.githubusercontent.com/99619460/184974030-abb709fb-f582-4d82-938d-80416dbed01a.png)

![image](https://user-images.githubusercontent.com/99619460/184973997-4669fe29-6384-4d2f-92be-abcb82fa9111.png)

##### 2.2.1.2. Logical Model
###### 2.2.1.2.1. ERD

![image](https://user-images.githubusercontent.com/99619460/184974224-d01e358b-6928-4dd4-9940-98f642e6bf39.png)

###### 2.2.1.2.2. Trigger Function
The database needs a trigger function as this facilitates the movement of data from the database to the data warehouse.

###### 2.2.1.2.3. Keys (Primary & Secondary)
All the tables have the primary and secondary key, so data can be indexed faster, assist with joins, and ensures consistency.

###### 2.2.1.2.4. Relationship
All the relationships between tables are defined to build structures and prevent redundant data.

###### 2.2.1.2.5. Transactional Data Timestamp
Each table has an Extraction Timestamp column, providing a log of each record when the data was extracted, transformed, and stored in the database.

##### 2.2.1.3. Physical Model
###### 2.2.1.3.1. ERD
Based on the physical model of below ERD relationships, keys and timestamps are defined.

![image](https://user-images.githubusercontent.com/99619460/184974605-aca58636-3fca-441b-b41f-4724a1cc4e40.png)

#### 2.2.2. Unstructured Data

##### 2.2.2.1. Table & Flowchart
Data is extracted via API, transformed, and loaded into the below tables in Postgres Database

![image](https://user-images.githubusercontent.com/99619460/184974815-aa6593fc-367b-4e69-8dbd-564c63c1a52c.png)

![image](https://user-images.githubusercontent.com/99619460/184974759-512d947b-1f34-4022-94f3-0709cd617f5f.png)

##### 2.2.2.2. Logical Model

###### 2.2.2.2.1. ERD

![image](https://user-images.githubusercontent.com/99619460/184975033-6e53d608-849d-4475-bfc6-456ae6340038.png)

###### 2.2.2.2.2. Keys (Primary & Secondary)
All the tables have the primary key so data can be indexed faster and ensures consistency.

###### 2.2.2.2.3. Transactional Data Timestamp
Each table has an Extraction Timestamp column, providing a log of each record when the data was extracted, transformed, and stored in the database.

##### 2.2.2.3. Physical Model 

###### 2.2.2.3.1. ERD
Based on the physical model of below ERD relationships, keys and timestamps are defined.

![image](https://user-images.githubusercontent.com/99619460/184975496-005c864f-a6ba-4d6c-a700-e8fd2c0d9acf.png)

### 2.3. Data Warehouse Design

#### 2.3.1. Table & Flowchart
All the data is imported via a trigger from the database except All Stats Fact. All Stats Fact table is imported from the database via Python framework.

![image](https://user-images.githubusercontent.com/99619460/184975860-d7c4cb2c-1734-42cb-a6c3-be73a5d077b0.png)

![image](https://user-images.githubusercontent.com/99619460/184975796-280ab8aa-a3cb-4843-a70a-3f65964e4c60.png

#### 2.3.2. Logical Model

##### 2.3.2.1. ERD

![image](https://user-images.githubusercontent.com/99619460/184976266-d6cd0012-98bd-4a9c-9bdd-c484c2eeca3a.png)

##### 2.3.2.2. Incremental ETL
All the data is incrementally loaded from the database to the data warehouse. This ensures to retain all the historical records and only process data that needs to process.

##### 2.3.2.3. Keys (Primary & Secondary)
All the tables have the primary and secondary key, so data can be indexed faster, assist with joins, and ensures consistency.

##### 2.3.2.4. Relationship
All the relationships between tables are defined to develop table structures and prevent redundant data.

##### 2.3.2.5. Transactional Data Timestamp
Each table has an Extraction Timestamp column, providing a log of each record when the data was extracted, transformed, and stored in the database.

##### 2.3.2.6. Schema
The Data warehouse is designed as a star schema with one dimension table and other fact tables.

#### 2.3.3. Physical Model
##### 2.3.3.1 ERD
Based on the physical model of below ERD relationships, keys, timestamps, and star schema are defined. All the data is moved from the database to the warehouse via the Postgres Trigger function.

![image](https://user-images.githubusercontent.com/99619460/184976578-65b7e129-d6e0-499d-83c8-b5ee57ede204.png)

##### 2.3.3.2. All Stats Fact Table
The Python framework moves all the data from the database to the data warehouse.

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_engineering_pipeline/all_stats_fact_table

Data Orchestration - Windows Task scheduler is running Python script at set intervals throughout the day.

## 3. Data Science/ML Pipeline
The below visual explains the data science/ml pipeline.

![image](https://user-images.githubusercontent.com/99619460/184977540-56588e61-126b-4385-b4da-fc8e232176b4.png)

### 3.1. Timeseries Pipeline

#### 3.1.1. Research Environment

The Data is extracted from the data warehouse used in the timeseries pipeline to predict future Bitcoin and Ethereum prices. The below process reflects how the time series model was implemented in the research environment.

Flowchart

![image](https://user-images.githubusercontent.com/99619460/184977648-5df2d662-e846-49aa-83b1-0fe98fc50264.png)

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_science_ml_pipeline/test_environment.ipynb

#### 3.1.2. Production Environment

The Data is extracted from the data warehouse and used in the time series pipeline to predict future Bitcoin and Ethereum prices. Predicted values are stored in the data warehouse for visualization. The below process reflects how the time series model was implemented in a production environment.

Flowchart

![image](https://user-images.githubusercontent.com/99619460/184982776-bc7c0483-31bf-4080-836e-18b2523b5dfb.png)

Python Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_science_ml_pipeline/production_environment

### 3.2. NLP Pipeline
#### 3.2.1. Flowchart

![image](https://user-images.githubusercontent.com/99619460/184982950-84a6d4fa-9066-4332-9e32-66eb90e11443.png)

#### 3.2.2. Scripts

Reddit Comments - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_science_ml_pipeline/reddit_comments

Twitter User Tweets - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_science_ml_pipeline/twitter_user_tweets

Crypto News - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_science_ml_pipeline/crypto_news

All the scripts runs automatically at set intervals throughout the day via Windows Task Scheduler.

## 4. Data Analytics/Data Visualization Pipeline

The below visual explains the data analytics/visualization pipeline.

![image](https://user-images.githubusercontent.com/99619460/184983797-96aeadaa-88f6-4797-a219-5e030a825be5.png)


### 4.1. Table & Flowchart

Below, analytical and ml tables are extracted from the data warehouse and database for data analytics/visualization.

![image](https://user-images.githubusercontent.com/99619460/184983879-718f097d-d4c8-4eb2-be5d-7872f432964d.png)

![image](https://user-images.githubusercontent.com/99619460/184983894-db854904-bfcf-4b6c-ae73-f80387eb4c4c.png)

### 4.2. Power BI Gateway

Power BI Gateway serves as a bridge between on-premises data, and Power BI. Power BI Gateway is connected to Postgres data warehouse to get the data and source it to Power BI.

### 4.3. Power Query

All the data is transformed and prepped for data aggregation. Below graphic shows how different queries are dependent. 

![image](https://user-images.githubusercontent.com/99619460/184983987-7941f192-9ab7-4ffd-8793-93b7601a5642.png)

M Scripts - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_analytics_visualization_pipeline/m_scripts

### 4.4. DAX

Below, measures are calculated using DAX in Power BI. All these measures are used for data analytics/visualization.

DAX Code - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/data_analytics_visualization_pipeline/dax

### 4.5. Data Modeling
The below visual shows only nine tables are part of the data model, and others are standalone tables. The data model helps to load, retrieve, and analyze extensive amounts of data which is crucial for Power BI visuals/dashboards to load quickly. 

![image](https://user-images.githubusercontent.com/99619460/184984639-e3dad46e-7381-49e5-bcca-004150058e39.png)

![image](https://user-images.githubusercontent.com/99619460/184984659-ae1a4ae1-bcf9-4230-afcc-68cd84a0168c.png)

### 4.6. Power BI Report

Below visuals show different reports created in Power BI.

![image](https://user-images.githubusercontent.com/99619460/184984804-933162ea-3287-42d8-9868-880080a3e765.png)

![image](https://user-images.githubusercontent.com/99619460/184984851-9a763e68-12c6-475d-ba41-057a39265dc9.png)

### 4.7. Power BI Dashboard

Below visuals show different dashboards created in Power BI.

![image](https://user-images.githubusercontent.com/99619460/184985050-6b34b42c-799c-4d7b-b19b-dbf2c15aa6c0.png)

![image](https://user-images.githubusercontent.com/99619460/184985074-77c0f1eb-fa7b-430f-b1b4-86bfc3b24634.png)

![image](https://user-images.githubusercontent.com/99619460/184985127-b970f567-c42e-4e69-9ef5-8dc24cca539f.png)

### 4.8. Power BI Service

Power BI Dashboard is hosted on the Power BI service. Below visual shows how the dataset is connected to the Power BI gateway and displayed via the Power BI dashboard.
 
![image](https://user-images.githubusercontent.com/99619460/184985236-fcbb1661-da69-42b6-9030-09b7467de443.png)

Data is refreshed every 3 hours.

![image](https://user-images.githubusercontent.com/99619460/184985270-9dba9367-ed0a-48cb-8e44-ee60bff7a901.png)

## 5. ML Engineering Pipeline

The below visual explains the machine learning engineering pipeline.

![image](https://user-images.githubusercontent.com/99619460/184985357-6b9ac63a-1e44-40d2-80b1-62671426bba9.png)

### 5.1. Streamlit Application

Power BI service provides an HTML link that can be used to embed the Power BI dashboard on any website. Streamlit is a Python framework that is used for building web applications. The Power BI dashboard link is
embedded inside the Streamlit application.

![image](https://user-images.githubusercontent.com/99619460/184985419-bae1b15b-8015-4373-9135-c4fe447cc23f.png)

### 5.2. Containerize Application

Docker helps package the Streamlit application file deployed to AWS for hosting.

![image](https://user-images.githubusercontent.com/99619460/184985485-750b1450-0a99-4c31-a325-2021b4ab8614.png)

Below files are used as part of containerizing the Streamlit application.

#### 5.2.1. Streamlit Application File

This file has the code for the Streamlit application.

Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/ml_engineering_pipeline/streamlit_application_file

#### 5.2.2. Docker File

Docker File is used for packaging the containerized Streamlit application.

Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/ml_engineering_pipeline/docker_file

#### 5.2.2. Requirement Txt File

Requirement Txt file is used for Python package dependency.

Script - https://github.com/Data-Practitioner/Crypto-Data-Metric/blob/main/ml_engineering_pipeline/requirement_txt_file

### 5.3. Deploy Application

Docker image file is uploaded AWS ECR → AWS ECR code is linked in AWS Fargate where the application is running → Cryptodatametric.com is domain is registered via Route 53 → AWS Fargate IP address is linked to Cryptodatametric.com so it will redirect traffic to the actual website rather than IP address.

![image](https://user-images.githubusercontent.com/99619460/184986236-3fcea828-abab-42aa-a64f-adf8275cb9f0.png)


## Conclusion

The project can be viewed at the below link.

Website ⇒ http://www.cryptodatametric.com:8501/

Below goals are completed. 

o  Descriptive Analytics – What is the price of Bitcoin and Ethereum? 

The dashboard displays the price of both along with changes from 1hour, 24 hours, and seven days ago.

![image](https://user-images.githubusercontent.com/99619460/184986318-34e21049-c625-4ba6-a8f3-dddfa090a2e8.png)

o  Diagnostic Analytics – Why is the price of Bitcoin and Ethereum going up or down? <br>
• Identify important social, on-chain, andgeneral statistical KPIs which affect the price. <br>
• Display the public’s sentiment on Bitcoin and Ethereum, which affect the price. <br>

The dashboard displays general, on-chain, social, and sentimental statistics that affect the price of Bitcoin.

![image](https://user-images.githubusercontent.com/99619460/184986471-38b88909-99a2-4bb8-bd67-c033af4395d3.png)

The dashboard displays general, on-chain, social, and sentimental statistics that affect the price of Ethereum.

![image](https://user-images.githubusercontent.com/99619460/184986496-359951d3-0672-44f3-9caf-c9baaa6f605f.png)

o  Predictive Analytics – What will be the future price of Bitcoin and Ethereum? 

The Dashboard displays the predicted price of Bitcoin and Ethereum.

![image](https://user-images.githubusercontent.com/99619460/184986537-58a05954-cc93-4f04-8f10-45b32c031377.png)

o  Prescriptive Analytics – What decision should be taken knowing the future price of Bitcoin and Ethereum? <br>
• Trading Signal – Buy or Sell. <br>

The dashboard displays the buy and sell trading signal on Bitcoin and Ethereum.

![image](https://user-images.githubusercontent.com/99619460/184986614-7528ebdf-f073-49f7-9ed2-bbef9019a94c.png)

o  Launch this product under the Crypto DataMetric domain. <br>
• Build the dashboard as a web application. <br>
• Link the web application to cryptodatametric.com. <br>

This is the main dashboard page where anyone can select Bitcoin or Ethereum to view its dashboard.

![image](https://user-images.githubusercontent.com/99619460/184986696-30c2a6b8-ad7a-46e0-9f4c-05e4ca110933.png)

Different layers of analytics for Bitcoin are captured in this single dashboard.

![image](https://user-images.githubusercontent.com/99619460/184986720-bca2c5b0-f08c-4958-8a06-13d04b8dfeb9.png)

Also, different layers of analytics for Ethereum are captured in this single dashboard.

![image](https://user-images.githubusercontent.com/99619460/184986749-099d96a8-3fa9-458d-a3ae-c955c5130231.png)

# Disclaimer
Crypto Data Metric is a fictional company; it was used to showcase a real-world project from a real company’s perspective. 
