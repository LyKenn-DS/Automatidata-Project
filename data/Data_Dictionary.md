# 2017 Yellow Taxi Trip Data table

| Column name | Description |
| --- | --- |
| ID | Trip identification number |
| VendorID | A code indicating the TPEP provider that provided the record. <br>&emsp; **1=Creative Mobile Technologies, LLC;** <br>&emsp; **2=VeriFone Inc.** |
| tpep_pickup_datetime | The date and time when the meter was engaged. |
| tpep_dropoff_datetime | The date and time when the meter was disengaged. |
| Passenger_count | The number of passengers in the vehicle. (Driver-entered value) |
| Trip_distance | The elapsed trip distance in miles reported by the taximeter. |
| PULocationID | TLC Taxi Zone in which the taximeter was engaged. |
| DOLocationID | TLC Taxi Zone in which the taximeter was disengaged. |
| RateCodeID | 	The final rate code in effect at the end of the trip. <br>&emsp; **1= Standard rate** <br>&emsp; **2=JFK** <br>&emsp; **3=Newark** <br>&emsp; **4=Nassau or Westchester** <br>&emsp; **5=Negotiated fare** <br>&emsp; **6=Group ride** |
| Store_and_fwd_flag | This flag indicates whether the trip record was held in vehicle memory before being sent to the vendor, because the vehicle did not have a connection to the server. <br> **Y= store and forward trip** <br> **N= not a store and forward trip** |
| Payment_type | A numeric code signifying how the passenger paid for the trip. <br>&emsp; **1=Credit card** <br>&emsp; **2=Cash** <br>&emsp; **3=No charge** <br>&emsp; **4=Dispute** <br>&emsp; **5=Unknown** <br>&emsp; **6=Voided trip** |
| Fare_amount | The time-and-distance fare calculated by the meter. |
| Extra | Miscellaneous extras and surcharges. Currently, this only includes the $0.50 and $1 rush hour and overnight charges. |
| MTA_tax | $0.50 MTA tax that is automatically triggered based on the metered rate in use. |
| Improvement_surcharge | $0.30 improvement surcharge assessed trips at the flag drop. The  improvement surcharge began being levied in 2015. |
| Tip_amount | Tip amount – This field is automatically populated for credit card tips. Cash tips are not included. |
| Tolls_amount | Total amount of all tolls paid in trip. |
| Total_amount | The total amount charged to passengers. Does not include cash tips. |

Refer to [NYC Open Data](https://data.cityofnewyork.us/Transportation/2017-Yellow-Taxi-Trip-Data/biws-g3hs/about_data) for more information related to this dataset.
