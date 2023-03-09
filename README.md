# Uber-Analysis
## Basic Description
This purpose of this project is to explore hired-ride trip data from Uber and NYC Yellow cab from January 2009 through June 2015, and joining with local historical weather data to find the some trends to back up why Uber and taxis have clashed for years. We first Preprocessed data by dropping null values, adjusting data types, calculating required numbers, and filtering the data needed. We then created and populated five tables: one for your sampled datasets of Yellow Taxi trips, one for Uber trips, one for hourly weather information, one for daily weather information, and one for daily sunrise and sunset information. Afterwards, we crafted a set of SQL queries to develop a better understanding of the datasets and created visualizations to enhance reader's understanding of the datasets.


## Part 1 

#### Calculating distance
- Define two functions to calculate the distance between pickups and dropoffs and add the trip distance data to the designated dataframe

#### Processing Taxi Data
- Generate a chart to refer location IDs to corresponding latitude and longitude
- Define two functions to programmatically download the Yellow Taxi trip data <br />
  *find_taxi_csv_urls()* & *get_and_clean_month_taxi_data()* 
- Define a function to process each month's yellow taxi data: filter the trips in the NYC area, drop unnecessary and null values, rename column names, append to the dataframe, and standardize the column types to desired format <br />
  *get_and_clean_taxi_data()*

#### Processing Uber Data
- Define a function to process Uber data: filter the trips in the NYC area, drop unnecessary and null values, rename column names, append to the dataframe, and standardize the column types to desired format <br />
  *load_and_clean_uber_data(csv_file)*
- Define a function to add a column that calculate trips distance <br />
  *def get_uber_data()*
  
#### Processing Weather Data
- Define a function to merge all weather files together and standardize the column types to desired format <br />
  *merge_weather_file()*
- Define two functions to extract houlry weather data and split the pickup date to Year, Month, Day <br />
  *clean_month_weather_data_hourly(csv_file)*
- Define a function to extract daily weather data and split the pickup date to Year, Month, Day <br />
  *clean_month_weather_data_daily(csv_file)*
- Define a function to store daily sunrise and sunset time 
  *clean_month_sun_data_daily(csv_file)*
  
## Part 2: Storing Cleaned Data

We used SQL schema to built five tables in project.db. The tables are named hourly_weather, daily_weather, yellow_taxi, weather_sun, and uber. The function write_dataframes_to_table is used to load and add the data to the tables.

## Part 3: Understanding the data 

In part 3, we used 7 SQL queries to develop 6 questions, which help us to understand the dataset.
  
## Part 4
- Define functions to create appropriate visualization 
