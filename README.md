# Google Data Analytics Professional Certificate: Case Study

## Business task:
Cyclistic, a bike-sharing company in Chicago, believes that maximizing the number of annual members will be key to future growth and would like to convert casual riders into members. To do such, I have been asked by the marketing department to analyze historical trip data to better understand how annual members and casual riders differ. These trends will give us more insight on why casual riders would buy Cyclist annual memberships and will ultimately help us achieve our business goal. From these insights, I will make recommendations on new marketing strategies to convert casual riders into annual members.

## Description of data sources used:
Cyclist is a fictional company but for the purpose of this case study, I am using public data made available by Motivate International Inc. (The raw data can be found here: https://divvy-tripdata.s3.amazonaws.com/index.html).This dataset is based on a real bicycle sharing service in the City of Chicago so it is credible data. Data-privacy issues prohibit me from using riders' personally identifiable information so we cannot determine if casual riders live in the Cyclist service area or if they have purchased multiple single passes.
I am specifically going to analyze the previous 7 months of Cyclist trip data to search for trends (November 2020- May 2021) using spreadsheets. (I originally wanted to try working with 12 months of data but the datasets for June-October 2021 were too large to upload to Excel Online and Google Sheets.) Each dataset is organized with 13 rows:
| ride_id | Unique id per ride |
| --- | --- |
| rideable_type | Type of bike used: electric bike, classic bike, or docked bike |
| started_at | Date and time |
| ended_at | Date and time |
| start_station_name | Name of station where ride began |
| start_station_id | Unique station id |
| end_station_name | Name of station where ride ended |
| end_station_id | Unique station id |
| start_lat | Starting location lattitude |
| start_lng | Stating location longitude |
| end_lat | Ending location lattitude |
| end_lng | Ending location longitude |
| member_casual | Type of member: member or casual |
