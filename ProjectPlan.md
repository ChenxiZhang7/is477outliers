# Final Project Plan
#### Team Outliers: Chenxi Zhang, Ethan Hung, Mustafa El Zayyat



## Overview: 

This project investigates whether a relationship exists between automated speed camera enforcement, traffic crash occurrences, and crash-related injuries in Chicago. Using three publicly available datasets from the Chicago Data Portal, Speed Camera Violations, Traffic Crashes – Crashes, and Traffic Crashes – People, we aim to identify spatial and temporal patterns that connect enforcement activity to crash frequency and injury outcomes across the city.

Our approach involves three main steps. First, we will clean and integrate the three datasets by linking crash records and person-level injury data through a shared Date field, and spatially matching speed camera locations to nearby crash events. Second, we will conduct exploratory data analysis to describe the distribution of violations, crashes, and injuries across time, location, and road user type, identifying high-risk zones and periods where enforcement activity and crash severity overlap.

By combining enforcement data with crash-level and person-level records, this project aims to provide evidence on how Chicago's automated speed enforcement program relates to traffic safety outcomes. The findings will contribute to a broader understanding of what factors most strongly predict crash occurrences and injuries, and may offer insights. 




## Team: 

  Our project team consists of three members, each responsible for managing one dataset and contributing to integration and analysis.

  Chenxi Zhang: Will work with the traffic crashes – crashes dataset and focus on cleaning and organizing crash-level event data, handling variables such as crash date, time, location, weather conditions, and contributing factors. I will be responsible for standardizing key fields and preparing the dataset for integration with other datasets using shared identifiers. I will assist in aggregating crash level information and aligning it with person level injury data and speed camera violations data through temporal and spatial matching. I will also collaborate with team members on analysis and data integration to ensure that the datasets are correctly linked and consistent across different levels of detail.

  Mustafa El Zayyat: Will work with speed camera violations dataset and focus on cleaning and organizing the time series data, handling variables such as camera ID, location, and daily violation counts. I would also be responsible for preparing spatial information (camera locations) if necessary and summarizing enforcement intensity over time and across locations. Will also collaborate with team members on analysis and data integration to ensure that the datasets are correctly linked using shared identifiers. 

  Ethan Hung: Will work with the traffic crashes people dataset and focus on cleaning and       organizing person-level crash data, handling variables such as person ID, person type (driver/passenger), crash record ID, vehicle ID, crash date, and demographic information. Also, I will standardize fields related to occupant safety and injury outcomes, including safety equipment usage, airbag deployment, ejection status, and injury classification. Moreover, I will collaborate with team members on analysis and data integration to ensure person-level records are correctly linked with other datasets using shared identifiers.



## Research or Business Question: 

Is there a relationship between speed camera violations, traffic crashes, and crash injuries in Chicago? (What factors are most strongly associated with traffic crash occurrences in Chicago?)



## Datasets:
  
   ### Dataset 1: Speed Camera Violations 
   - Source: Transportation Security Administration (TSA)
    
   - Dataset: TSA Checkpoint Travel Numbers
    
   - Link: https://www.tsa.gov/travel/passenger-volumes
   
   - Variables: Date, Passenger throughput (# of passengers screened)
   
   - Description: This dataset reports the number of passengers moving through TSA airport security checkpoints each day in the United States; passenger throughput can be used as a proxy for airline travel demand because most commercial airline passengers pass through TSA screening before departure. Also, for this project, we will use data from 2021 to 2026 to align with the fuel price and airline ticket price           datasets. Moreover, because the fuel and ticket price data will be analyzed at a monthly level, the daily TSA data will likely be aggregated into monthly passenger totals or averages for integration.
   
  ### Dataset 2: Jet fuel prices in past 5 years (Mustafa)
    
  - Source: U.S. Energy Information Administration (EIA) via Federal Reserve Economic Data (FRED)
  
  - Dataset: Kerosene-Type Jet Fuel Prices: U.S. Gulf Coast (DJFUELUSGULF)
  
  - Link: https://fred.stlouisfed.org/series/DJFUELUSGULF
  
  - Variables: Jet fuel price (Dollars per gallon) and Date
  
  - Description: This dataset provides daily spot prices for kerosene-type jet fuel in the U.S. Gulf Coast market, which is one of the primary fuel pricing benchmarks used by airlines in North America. The dataset is reported in dollars per gallon and is not seasonally adjusted. For this project, we will focus on the last five years of data (2021–2026) to analyze recent pricing dynamics. Because airline ticket pricing data is typically available at a monthly or quarterly frequency, the daily fuel price observations might need to be aggregated to a monthly average to enable integration with other datasets.

  ### Dataset 3: Airline Ticket Prices (Chenxi)
  
  - Source: U.S. Bureau of Labor Statistics (BLS) via Federal Reserve Economic Data (FRED)

  - Dataset: Consumer Price Index for All Urban Consumers: Airline Fares in U.S. City Average 

  - Link: https://fred.stlouisfed.org/series/CUUR0000SETG01

  - Variables: Airfare price index (Consumer Price Index) & Date

  - Description: This dataset provides a monthly index for measuring changes in air ticket prices in the United States. These data are from the consumer price index (CPI) released by the Bureau of Labor Statistics of the United States and are published through the Federal Reserve's Economic Data (FRED) database. The air ticket price index reflects the average price trend of air tickets purchased by consumers in American cities. In our project, the dataset will be used to represent the overall trend of air ticket prices in the US market. Since the data is reported monthly, it can be easily integrated with other data sets. By combining jet fuel price data and passenger demand data, this dataset will help analyze how fluctuations in fuel costs and travel demand affect air ticket pricing over time.




## Timeline:

### Phase 1: Project Planning (Before Apr 12)

1.	Finalize research question related to fuel prices, passenger demand, and airline ticket prices.
2.	Find appropriate datasets from reliable sources.
3.	Review the structure of the datasets and confirm that they can be combined.
4.	Set up the GitHub repository and organize the project files.
5.	Prepare and submit the project plan.

### Phase 2: Data Cleaning and Integration (March 13 – March 31)

1.	Collect the datasets related to airline ticket prices, passenger demand, and jet fuel prices.
2.	Review the datasets to understand their structure and check for potential issues.
3.	Clean the data, like handling missing values or adjusting formats.
4.	Combine the datasets using shared attributes such as time period.
5.	Create some charts or summary statistics to explore the data.
6.	Write and submit the Status Report.

### Phase 3: Analysis and Final Project (April 1 – May 3)

1.	Further analyze the relationship between fuel prices, ticket prices, and passenger demand.
2.	Create visualizations to show important trends and patterns.
3.	Prepare scripts that organize the data processing steps.
4.	Document the data cleaning process and analysis workflow.
5.	Write the final project report and organize the repository.
6.	Submit the Final Project.



## Constraints:

Some restrictions may affect the scope and interpretation of our analysis.

### Different Levels of Detail Across Datasets
One challenge in this project is that the three datasets are structured at different levels. The Traffic Crashes – Crashes dataset records information about each crash event, the Traffic Crashes – People dataset records information about every individual involved in a crash, and the Speed Camera Violations dataset records the number of violations per camera on each day. Because multiple people can be involved in a single crash, the people dataset must therefore  be aggregated to the crash level using CRASH_RECORD_ID before it can be compared with crash events and enforcement data. Also, linking crashes to speed camera activity will also require matching records based on date and approximate location, since crashes are not recorded directly at camera locations.
 
### Differences in Time and Location Information
Another limitation is that the datasets record time and location in different ways; speed camera data reports the total number of violations per camera per day, while crash data includes more detailed timestamps and addresses. Thus, to make the datasets comparable, crash records may need to be grouped at the daily level, which reduces some of the detail in the crash timing. In addition, crashes and cameras do not share a common geographic identifier, so crashes will need to be matched to nearby cameras using location information; this means the relationship between enforcement zones and crashes can only be estimated.

### Data Quality and Missing Information
Some variables in the crash and people datasets contain missing or unclear values. Fields such as injury classification, safety equipment use, driver vision, and contributing factors often contain entries like “UNKNOWN” or “NOT APPLICABLE.” As a result, these values can limit certain analyses or require us to filter or group categories during data cleaning. Also, in some cases, the information in crash reports is based on the reporting officer’s assessment at the time, which may lead to inconsistencies across records.
 
### Limits of the Data for Explaining Causes
Finally, the datasets do not directly measure overall traffic exposure or driving behavior; the speed camera dataset records violations detected by cameras, but this does not necessarily reflect all speeding activity in an area. Similarly,  crash records show where crashes occurred but do not include factors like traffic volume. Because of this, the project can identify patterns and relationships between enforcement activity, crashes, and injuries, but it cannot entirely determine whether speed cameras cause changes in crash outcomes.



## Gaps:

One area that could be considered a gap is the disparity in the datasets' levels of detail. The crash dataset is at the event level, the speed camera data is arranged by camera and day, and the person's dataset is at the individual level. Our team will have to choose a consistent unit of analysis and aggregate the person level data to match crash level or location level data in order to draw meaningful comparisons.

Another significant area is data quality gaps, such as incomplete or missing values in categories like the severity of injuries, the use of safety equipment, and demographic data. These problems will require us to make choices regarding missing data processing or filtering. Furthermore, it is still necessary to specify important variables and metrics, such as how to define crash frequency, injury severity, and enforcement.
