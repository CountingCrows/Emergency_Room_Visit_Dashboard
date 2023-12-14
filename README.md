# Emergency_Room_Visit_Dashboard

## Overview
I've created an interactive dashboard with Tableau Public for a Project named Emergency Room Dashboard. The dataset used is Hospital ER from [RWFD](https://data.world/markbradbourne/rwfd-real-world-fake-data/workspace/file?filename=Hospital+ER.csv) where it contains data from 2019 to 2020. 

The Case of this project is that we want to know how patients show up to the emergency room in a span of a time. This can help us to gain various insights to then make decisions or recommendations for the hospital.

Columns to point out:
- patient id, is like a social security number. In the real case we can use a random generated primary key
- patient satisfaction score in a scale 0-10
- patient wait time -> number of minutes that the patient was waiting to get treated in the emergency department
-  Department Referral is what specialty got involved in the treatment of that patient in the emergency room, so for example if a senior citizen slipped and broke their hip, their might be a situation where the Orthopedics will get involved. High Fever can maybe be General Practice.

## Graphs
- Number of times there is a patient in this data set which represents an emergency room encounter. The count of patient ID that's going to represent how many encounters in the emergency room we have over this span of time 
- The percentage of how many patients in each gender did we see in the emergency room over the span of time
- Patient Satisfaction, a line chart of the average of patient satisfaction score over the span of time
- Patient Waittime, a line chart the average of patient wait time over the span of time
- Average Satisfaction, the overall average of patient satisfaction
- Average Waittime, the overall average of patient waittime
- Number of Patients by Age, making a line chart of patient ID and grouping them by a calculated field named Age Grouping
  - Age Grouping, creating a calculated field where we want to group our patients age from 0-18, 19-65, and 66 and above. 
IF [Patient Age] >= 0 and [Patient Age] <=10 then '0-18'
ELSEIF [Patient Age] >= 19 and [Patient Age] <=65 then '19-65'
ELSEIF [Patient Age] >= 66 then '66+'
END
- Average Wait Time Heatmap, a heatmap to see the average wait time for every hour in every weekdays. each cell can tell us a pattern to our data.
- Patient Race, a bar chart that will show us the number of patients belonging to a certain race that was in the emergency department
- Dept Referral, a bar chart that will show us which departments that was reffering the patients.


### You can visit the interactive dashboard [here](https://public.tableau.com/views/EmergencyRoomDashboard_16996883660300/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link)
