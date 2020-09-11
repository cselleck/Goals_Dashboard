# Goals_Dashboard

## Project Summary

At my current job, we have a Tableau dashboard that shows our progress towards our sales and referral goals. While it is useful, there are some metrics that I feel that would be very useful that are either missing, or displayed in an inefficient manner. This is my attempt to make a dashboard from the user's perspective. In the words of somebody famous that I don't really remember: "Be part of the solution, not part of the problem."

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
