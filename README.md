# REAL ESTATE OPPORTUNITY <br>

# Summary
You are competing in a new real estate market. The objective is to break into the market by capitalizing on short term and long term leasing for international markets in the US targeting students and  business travelers. More specifically, the following points for real estate and business forecasting.:

* Determine what country of residency people has the most amount of people coming in daily, monthly, yearly?
* What states are they arriving at?
* In the state they are arriving at what is the demographics?

These points will help the marketing team better market towards countries where people are forecasted to travel to the US and also, forecast how many estates they have to get on their sites to meet the demands.

The project follows the follow steps:
* Step 1: Scope the Project and Gather Data
* Step 2: Explore and Assess the Data
* Step 3: Define the Data Model
* Step 4: Run ETL to Model the Data
* Step 5: Complete Project Write Up


# Scope
In this project we are going to extract data from the data sources listed above using ApacheSpark for scalable data in order to create and ETL that organizes the data in a star-schema for the team. For smaller data sources we will be using Pandas dataframe.

# How to run the code
You have to open the jupyter notebook and just run the code. Make sure all proper packages
are installed.


# Describe and Gather Data

To accomplish this study the following data sets were used:

* **I94 Immigration Data**: This data comes from the US National Tourism and Trade Office. A data dictionary is included in the workspace.
   * country_code.csv: table contains country codes used in the dataset extracted from the data dictionary.
   * iport_data.csv: table contains airport codes associated with city codes extracted from the data dictionary.

* **U.S City Demographic Data**: This dataset contains information about the demographics of all US cities and census-designated places with a population greater or equal to 65,000. This data comes from the US Census Bureau's 2015 American Community Survey.

* **Airport Code Table**: This table has airport codes corresponding to muncipals and states.

#schema
Since the scope of this project is to forecast future travel from foreign countries to the US, the aggregated immigration data will be the fact table.
​
**Fact Immigration** will be:
* immigration_id         (Primary Key)
* gender_id              
* arrival_date           
* i94res                 
* i94port              
* i94visa:         
* term             
​
​
​
For the dimension tables there are going to be 4 dimension tables:
​
 **dim_date**
* arrival_date (Primary Key)
* year
* month
* day
* week
* weekday
* dayofyear
​
**dim_airport**
* i94port  (Primary Key)
* city
* state_code
​
**dim_visa**
* i94visa  (Primary Key)
* visa
​
**dim_gender**
* gender_id  (Primary Key)
* gender
​
​
The following is a seperate schema that shares the dim_destination table but prioritizes demographics information for research on estate owners in the area. It uses the fact table **fact_demographics**.
​
**fact_demographics**
* city_id  (compound primary key (city, state)
* race
* race_count
​
**dim_city**
* city_id  (Primary Key)
* city
* state
* state_code
* Female Population
* Male Population
​
​
​
# Relational Database
![Image description](img/schema.PNG)





## Build Status <br>

 The project has been completed and ready for deployment. <br>

 ## Code Style <br>

 Standard. <br>
