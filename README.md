# Google Data Analytics Professional Certificate: Case Study

## Business task:
Cyclistic, a bike-sharing company in Chicago, believes that maximizing the number of annual members will be key to future growth and would like to convert casual riders into members. To do such, I have been asked by the marketing department to analyze historical trip data to better understand how annual members and casual riders differ. These trends will give us more insight on why casual riders would buy Cyclist annual memberships and will ultimately help us achieve our business goal. From these insights, I will make recommendations on new marketing strategies to convert casual riders into annual members.

## Description of data sources used:
Cyclist is a fictional company but for the purpose of this case study, I am using public data made available by Motivate International Inc. (The raw data can be found here: https://divvy-tripdata.s3.amazonaws.com/index.html). This dataset is based on a real bicycle sharing service in the City of Chicago so it is credible data. Data-privacy issues prohibit me from using riders' personally identifiable information so we cannot determine if casual riders live in the Cyclist service area or if they have purchased multiple single passes.
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

## Documentation of any cleaning or manipulation of data:
To ensure my data's integrity I first questioned all the blank cells found in my datasets. If I was given this task in an interview/job I would have asked the project manager if these records are errors that should be deleted before I conduct my analysis. However, after realizing all 7 datasets had large amounts of blank cells in the "start_station_name", "start_station_id", "end_station_name", and "end_station_id" columns, I suspected there was a reason for this lack of information, which I looked into before deleting these rows from the datasets. Sure enough, after filtering my spreadsheet, I realized that only electric and classic bikes had empty cells in these columns. My case study mentioned that Cyclistic bikes can be "unlocked from one station and returned to any other station in the system anytime" but the data shows that a large amount of users (both casual riders and members) are starting and ending their electric bike rides at non-station locations. Since the dataset for this project is from a real bike-sharing company, Divvy, I did further research and realized that while it is recommended "ebikes be returned to an e-station", ebikes can be docked and picked up anywhere with a provided cable lock and pin. (Sources: https://help.divvybikes.com/hc/en-us/articles/360033122072-How-to-dock-a-bike, https://help.divvybikes.com/hc/en-us/articles/360033122012-How-to-start-a-ride). This ensured me that the datasets were accurate and the large amount of blank cells were not a result of errors. To further ensure my data's integrity, I also calculated the trip duration time for each instance and checked if any values came out negative using spreadsheets' "COUNTIF" function and filtering. By checking the duration value, I discovered that some values in the started_at and ended_at columns were incorrect since some bike rides ended before they even began. Since I was unsure of the error's cause, I deleted rows that returned a negative duration value. If I was given this case study at an interview or job, I would have asked my project manager before deleting rows. After ensuring my data's integrity, I began the cleaning and transformation process which is described in the attached change log.
[Change Log Trip Data.txt](https://github.com/yerlineUCI/Case-Study/files/7681086/Change.Log.Trip.Data.txt)

## Summary of Analysis
My data is organized by month so I will analyze each month individually and then compare results to get an overall view of the 7-month span. I first added a few calculations to each dataset to get a better sense of the data layout. These calculations include the mean, max, and min of the ride_length column and the mode for the day_of_week column. I then created pivot tables for each dataset to calculate and visualize the data. I used pivot tables to calculate the average ride_length for members and casual riders, the number of rides for users by day_of_week, the mode of day_of_week for members and casual riders, the average ride_length for users by day_of_week, and the amount of unique starting and ending stations for members and casual riders. By using these techniques I came up with the following conclusions:

* Members use the bikes more often than casual users, but casual users use bikes for much longer time intervals. This is most likely because members are currently mostly using the bike sharing service as a main source of transportation while casual users are using it recreationally. However, both members and casual users prefer the flexibility of dropping off and picking up the bikes anywhere rather than using the docking stations. As a result, less customers are actually using the docking station and purchasing their passes there. This means that casual users are actually using the the bike sharing app to buy their pass.
