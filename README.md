# Goals_Dashboard

## Project Summary

At my current job, we have a Tableau dashboard that shows our progress towards our sales and referral goals. While it is useful, there are some metrics that I feel that would be very useful that are either missing, or displayed in an inefficient manner. This is my attempt to make a dashboard from the user's perspective. In the words of somebody famous that I don't really remember: "Be part of the solution, not part of the problem."

## Goals of the Project

My goal is to create an interactive dashboard that not only shows the progress in goals to date, but also projects what the year-end results would be based on the current trends, and to offer solid data on how to acheive a satisfactory end of year result (e.g. current projected EOY Auto Referrals = 143; Goal Year to date is 200; to meet goal, you would need an extra 3 referrals per week to meet goal, and 5 extra to meet the exceeds category)

## Methods

Obviously, I don't have access to the company's database in the position I currently have. I created my own dataset in excel, making a few assumptions:
* The records for my dashboard are the result of a query for my information only; meaning I don't need to separate my results from the team's.
* The total team results are stored in a discrete table for ease of reporting.
* Days that contain no MSI (or customer satisfaction surveys) results are represented with a null value.
* Days that contain no sales or referrals are represented with a 0.
* My Tableau data link is set to extract rather than continuous- I am assuming the reports do not update in real time, but at specific intervals set by internal processes.
* All numeric values are stored as numbers and not strings.
* Monthly and annual goals are stored internally and can be referenced by Tableau.
* Phone metrics and time management are each stored on separate tables, as they originate from different applications.

Please note that all the data is completely fictional- any correlation to your own progress is purely coincidental, and possibly cause for concern.

### The Data Set

I created an excel workbook with several tabs, to represent my best guess as to how the company database is set up. I have one table for the basic goals. One thing of note- I know that the MSI scores are recorded separately, but I included them in the main workbook purely for my own convenience. I have another tab for the phone metrics, and a third for the Time management information. I also have a fourth that includes monthly and yearly goals.

For the purposes of this project, I assume today is Sept 15, 2020. This allows me to calculate fields based on the current date, without having to add more data to my dataset every day. In real life, the database queries would update based on the actual date.

The MSI percentage may be calculated within the database, but for the purposes of this project I assumed that only the raw score is included.

To account for business holidays, I downloaded a separate excel file that contains all US holidays, and removed all that did not result in a closure of business. The dataset is through 2099- after that it becomes somebody else's problem. This dataset also allowed me to filter for Saturdays and Sundays. Although the business is open on Saturday, the number of hours worked for an employee is always 40- the equivalent of a 5 day work week. For the business days in the month calculations, I excluded the weekends entirely. I did include Saturday sales in my sum calculations.

