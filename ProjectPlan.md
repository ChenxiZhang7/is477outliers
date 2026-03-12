Overview: 

The goal of this project is to analyze how airline ticket prices change in relation to jet fuel prices and demand related factors. Airline pricing is influenced by many variables, including operational costs (such as  jet fuel), consumer demand, seasonality, and broader economic conditions. Jet fuel is one of the largest variable costs for airlines, so fluctuations in fuel prices may influence ticket pricing strategies. Our project will investigate whether increases or decreases in jet fuel prices and customer demand are associated with changes in airline ticket prices over the past five years. In addition, we will incorporate demand related indicators such as passenger volumes to better understand how supply and demand interact with cost pressures in determining prices. To accomplish this, we will collect multiple datasets that can be linked by common attributes. These datasets will include airline ticket price data, jet fuel price data, and passenger demand metrics. We will clean and standardize the data, integrate the datasets into a unified structure, and conduct exploratory data analysis to identify trends, correlations, and potential lag effects between fuel prices, demand, and ticket prices.The final analysis will include visualizations and statistical summaries that illustrate the relationships between these variables and provide insight into how airline pricing responds to changes in cost and demand conditions.

Team: 

  Our project team consists of three members, each responsible for managing one dataset and contributing to integration and analysis.

  Fuel Cost Analysis (Mustafa): Collect and process the jet fuel price dataset, Clean and format fuel price data, Preparing the dataset for integration with other datasets

  Ticket Price Analysis (Chenxi): Responsible for collecting airline ticket price data, Cleaning price data and ensuring consistent formatting, Aggregating ticket prices by time period, Preparing dataset for integration

  Demand and Passenger Data Analysis (Ethan): Responsible for collecting airline demand data (e.g., passenger counts or load factors), Cleaning and preparing passenger demand dataset, Standardizing time variables, Assisting with final integration and visualization


Research or Business Question(s): 

How do fuel prices and passenger demand influence airline ticket prices and flight volumes in the U.S. airline market?

Datasets:
  
    Dataset 1: Flight Operations / Passenger Demand (Ethan)
    
    Source:
    
    Dataset:
    
    Link:
    
    Variables: 
    
    Description:
  
    Dataset 2: Jet fuel prices in past 5 years (Mustafa)
    
    Source: U.S. Energy Information Administration (EIA) via Federal Reserve Economic Data (FRED)
    
    Dataset: Kerosene-Type Jet Fuel Prices: U.S. Gulf Coast (DJFUELUSGULF)
    
    Link: https://fred.stlouisfed.org/series/DJFUELUSGULF
    
    Variables: Jet fuel price (Dollars per gallon) and Date
    
    Description: This dataset provides daily spot prices for kerosene-type jet fuel in the U.S. Gulf Coast market, which is one of the primary fuel pricing benchmarks used by airlines in North America. The dataset is reported in dollars per gallon and is not seasonally adjusted. For this project, we will focus on the last five years of data (2021–2026) to analyze recent pricing dynamics. Because airline ticket pricing data is typically available at a monthly or quarterly frequency, the daily fuel price observations might need to be aggregated to a monthly average to enable integration with other datasets.
  
    Dataset 3: Airline Ticket Prices (Chenxi)
    
    Source: U.S. Bureau of Labor Statistics (BLS) via Federal Reserve Economic Data (FRED)

    Dataset: Consumer Price Index for All Urban Consumers: Airline Fares in U.S. City Average 

    Link: https://fred.stlouisfed.org/series/CUUR0000SETG01

    Variables: Airfare price index (Consumer Price Index) & Date

    Description: This dataset provides a monthly index for measuring changes in air ticket prices in the United States. These data are from the consumer price index (CPI) released by the Bureau of Labor Statistics of the United States and are published through the Federal Reserve's Economic Data (FRED) database. The air ticket price index reflects the average price trend of air tickets purchased by consumers in American cities. In our project, the dataset will be used to represent the overall trend of air ticket prices in the US market. Since the data is reported monthly, it can be easily integrated with other. By combining jet fuel price data and passenger demand data, this dataset will help analyze how fluctuations in fuel costs and travel demand affect air ticket pricing over time.


Timeline:


Phase 1: Project Planning and Dataset Selection (March 1 – March 12)

1.	Finalize research question related to fuel prices, passenger demand, and airline ticket prices.
2.	Find appropriate datasets from reliable sources.
3.	Review the structure of the datasets and confirm that they can be combined.
4.	Set up the GitHub repository and organize the project files.
5.	Prepare and submit the project plan.


Phase 2: Data Cleaning and Integration (March 13 – March 31)

1.	Collect the datasets related to airline ticket prices, passenger demand, and jet fuel prices.
2.	Review the datasets to understand their structure and check for potential issues.
3.	Clean the data, like handling missing values or adjusting formats.
4.	Combine the datasets using shared attributes such as time period.
5.	Create some charts or summary statistics to explore the data.
6.	Write and submit the Status Report.


Phase 3: Analysis and Final Project (April 1 – May 3)

1.	Further analyze the relationship between fuel prices, ticket prices, and passenger demand.
2.	Create visualizations to show important trends and patterns.
3.	Prepare scripts that organize the data processing steps.
4.	Document the data cleaning process and analysis workflow.
5.	Write the final project report and organize the repository.
6.	Submit the Final Project.


Constraints:

Gaps:
