# Python-Data-Analytics-Project:

**Course:** [Google Advanced Data Analytics Professional Certificate](https://www.coursera.org/professional-certificates/google-advanced-data-analytics) 

## Scenario
I am assuming to be a junior data professional at Automatidata Consulting, whose focus is to help clients from The New York City Taxi & Limousine Commission (TLC) to develop an innovative application that provides riders with accurate, upfront taxi fare estimates. By leveraging extensive historical taxi trip data from TLC's vast network of taxi cabs and for-hire vehicles, we aim to enhance transparency, build trust, and ultimately improve the overall experience for millions of daily commuters in New York City. My initial task involves conducting a thorough Exploratory Data Analysis (EDA) to gain a foundational understanding of taxi ridership patterns, paving the way for the development of a robust fare estimation model. 

## Part I - Exploratory Data Analysis (EDA) and Data Wrangling
In order to gain clear insights and answer key business questions, New York TLC's data needs to be analyzed following the process: Ask, Prepare, Process, Analyze, Share, and Act.

#### (Data Wrangling) 
1. Initial Data Loading & Inspection
   - Loaded the raw taxi trip dataset into a Pandas DataFrame.
   - Before working on the data, I familiarized myself with the data by conducting profiling and computing summary statistics on each variable to find any inconsistencies.
2. Handling duplicate, missing, and outlying data
   - With each record assigned a unique id, partial duplicate rows were checked using only a subset of columns.  
   - Assessed the extent of outlying values across all columns.
   - Depending on its implication to project analysis, strategies such as capping values, removing extreme outliers, or noting their presence were applied to prevent skewed analysis. *Details of specific outlier handling will be noted in the Python notebook*
3. Data Type Conversion
   - Converted `pickup_datetime` and `dropoff_datetime` columns to datetime objects for time-based math and aggregations.
   - Ensured numerical and categorical columns were optimized to their appropriate data types.
4. Feature Engineering
   - Included `timelapse` column for ride duration for better understanding of the standard rate calculation.
   - Extracted granular temporal features (hour_of_day, month, day_of_week) from `pickup_datetime` to facilitate time-series analysis. 
6. Consistency Checks & Data Validation
   - Verified logical consistency (eg. standardizing the system of measure)
   - Checked for zero and negative values in columns where positive values are expected, provided there is a fare amount incurred. 

#### (Exploratory Data Analysis)
The analysis questions: <br>
&emsp;1. **Volume & Frequency -** *How many rides are there on average per day, week, and month?* <br>
&emsp;2. **Temporal Patterns -** *When are our busiest times? Are there specific date, time or seasons where demand spikes or dips significantly?* <br>
&emsp;3. **Geographical Hotspots -**  *Where are people picking up and dropping off most frequently?*  <br>
&emsp;4. **Ride Characteristics -**   *What's the typical length of a ride? How much is a typical fare?* <br>
&emsp;5. **Passenger Load -**   *How many passengers are usually in our taxis?* <br>
&emsp;6. **Payment Trends -**  *How are most people paying for their rides?* <br>

* [View Python Code](https://github.com/LyKenn-DS/Automatidata-Project/blob/63db242ead5f5b7dec7fd68241d67978e49f0f5e/Complete-Exploratory-Data-Analysis.ipynb)
* [Raw Dataset](https://github.com/LyKenn-DS/Automatidata-Project/blob/63db242ead5f5b7dec7fd68241d67978e49f0f5e/data/2017_Yellow_Taxi_Trip_Data.csv)
* [Cleaned Dataset](https://github.com/LyKenn-DS/Automatidata-Project/blob/63db242ead5f5b7dec7fd68241d67978e49f0f5e/data/Clean_2017_Taxi_Trip_data.csv)

### Insights Report: Automatidata NYC Taxi Trip Analysis   

[![NYC Taxi Ridership](https://github.com/user-attachments/assets/2c558d14-c558-4f46-ac05-81b66f1c17ba)](https://public.tableau.com/views/2017_NYC_Taxi_Trips/NYCTaxiRidership?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
This analysis reveals several key patterns:
* **Short Trip Dominance & Concentrated Drop-offs:** Most trips are short distances, with a rapid decline in frequency as distance increases. Furthermore, a disproportionate number of drop-off locations receive the majority of traffic, likely concentrated around popular tourist attractions, airports, and transportation hubs.
*  **Consistent Demand Fluctuations:** Demand is relatively stable during working hours, surges in the late afternoon/early evening (6-7 PM), and significantly drops after midnight.
*  **Weekday Peak:** Weekdays (Wednesday-Saturday) see higher ride volumes than weekends, likely reflecting work schedules and leisure travel.
*  **Seasonal Variations:** Rides and revenue dip during summer months (July-September) and February, potentially due to seasonal factors.
*  **Consistent Tipping:** Tips typically constitute 10-12% of driver revenue, with slightly higher tips observed for longer distances and during early morning hours when availability is lower.
*  **Cost and Tip Distribution:** Trip costs and tips exhibit right-skewed distributions, with a majority of rides falling within a specific price range.

These insights suggest opportunities for taxi companies & drivers to improve their operations, enhance customer satisfaction, and increase gross revenue by optimizing their operation schemes and resource allocation in an increasingly competitive transportation market.  

### Recommendations:
*  **Dynamic Pricing:** Implementing dynamic pricing strategies based on time, day, distance, and even drop-off location can optimize driver earnings and passenger demand.
*  **Fleet Management:** Optimizing fleet size and driver schedules to align with demand fluctuations and concentrate resources around high-traffic drop-off locations can improve service efficiency.
*  **Service Enhancements:** Identifying and addressing potential service gaps, such as improving availability during peak hours and early mornings, can enhance customer satisfaction.
*  **Flexible Payment Methods:** Offering a variety of popular payment options, such as direct debit, e-wallet, and book now pay later can improve customer trust as it allows them to enjoy the convenience and rewards that come with spending using a typical payment method.

## Part II - A/B Testing  
![image](https://github.com/user-attachments/assets/44cd78fe-2999-46db-9086-aeefa59ecd05) <br>
Based on the averages shown, it appears that customers who pay with credit card (1) tend to pay a larger amount than customers who pay with cash (2). By using AB Testing, I can determine the genuity about user behavior and promote more forms of digital credit options backed with compelling insight. 

* [View Python Code](https://github.com/LyKenn-DS/Automatidata-Project/blob/295854b7e453959ec9690f30d7abdd7dafe0bf42/Statistical_Test.ipynb)

## Part III - Linear Regression Analysis
In this project, I developed a robust linear regression model using Python's Scikit-learn library. Leveraging the comprehensive dataset, the supervised model was carefully constructed to not only provide precise fare estimates but also to identify as well as quantify the impact of key variables on the fare structure of NYC taxi cabs and for-hire vehicles.

* [View Python Code](https://github.com/LyKenn-DS/Automatidata-Project/blob/613158e1768ab9263feca0b213a2b087b2979944/Regression-Predictions.ipynb)

## Part IV - Model Classification 
To help improve the revenue for taxi cab drivers, I have also built a machine learning classification model in a project that will reliably classify generously tipping customers. 
This model can be integrated into an application that will notify taxi drivers of these potential high-tipping opportunities, directly contributing to improved driver revenue and operational efficiency.  

* [View Python Code](https://github.com/LyKenn-DS/Automatidata-Project/blob/896fe52b528bbbc5b4f8654715a1b65547660921/Classifier.ipynb)
