### Tableau Homework – CitiBike Analytics
### ........................................aka..............................................
### A Tale of Two Phenomena for Jersey City CitiBikes

![image](https://user-images.githubusercontent.com/89948865/163308462-74031ce2-3004-4207-ba6e-151752d2764e.png) 

Check out my Story at my Tableau Public Website
https://public.tableau.com/app/profile/michael.mike.murphy#!/?newProfile=&activeTab=0
 
### Background
My job is as the new lead analyst for the New York Citi Bike Program. I am responsible for overseeing the largest bike sharing program in the United States. In my new role, I am expected to generate regular reports for city officials looking to publicize and improve the city program.
Since 2013, the Citi Bike Program has implemented a robust infrastructure for collecting data on the program's utilization. Through the team's efforts, each month bike data is collected, organized, and made public on the Citi Bike Data webpage.
However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have a number of questions on the program. 

My first task on the job is to build a set of data reports to provide the answers to several questions by structuring and analysing the data. 

### The Task 

1. Aggregate the data found in the Citi Bike Trip History Logs and find two unexpected phenomena.
2. Design 2-5 visualisations for each discovered phenomenon, (4-10 total). I may work with a timespan of my choice and, optionally, may merge multiple datasets from different periods.
3. The following are some questions I may wish to tackle; however, I need not limit myself to these questions. They are suggestions for a starting point. I am encouraged to be creative. 

### Tackling the Task 

#### Time span chosen:	January to December 2020 

#### Created a Jupyter Notebook to do the following:
1. used  pd.concat combine the 12 csv files for each month of 2020 into a single csv to analyse in Tableau,
2. performed data cleansing as to minimise processing requirements for Tableau as the raw data has some inherent issues:
* 2.1 for example, “trip duration” is  too granular; it is recorded in seconds and was converted to minutes, 
* 2.2 simplified the scientific notation for the numeric data converting it to two decimal place notation, 
* 2.3 “starttime” and “stoptime” are loaded as data type object and were converted to timestamp format (object data types take up ten times as much memory as integer or float types which can be a problem in very large data sets like those encountered in Citi Bikes), 
* 2.4 reduced the amount of memory used for some of the other columns by using the category data type. (Categories are useful when there are a limited number of unique values for a column compared to the number of rows. The actual values are stored just once, and instead of storing a long string in each row, just an integer is stored that points to the actual value. The combined CitiBike file contains some 337,000 rows, but there are only some 1,600 unique “start and end station” so they are good candidates to store as categorical data. The “usertype” column with only two unique values should get similar treatment, as should “gender” with three values. Bikeid could also be treated similarly. 
3. Note that the number of rows was increased by a factor of 4 to assess Tableau’s capacity to handle big data. (I was encouraged to be creative.) 
4. created a distance column to simplify getting trip distance in Tableau. 
 
#### Used Tableau to satisfy the requirements of the assignment by: 
1. Analysing the Citi Bike Trip History Logs and finding two unexpected phenomena, 
2. Designing visualisations for each of the unexpected phenomena, 
3. Creating dashboards, a story board, and an official New Jersey city map as requested. 

### Two Unexpected Phenomena

#### The two unexpected phenomena discovered while using Tableau to analyse and visualise the trip history data were:
#### 1.	“Lap Trips”: so named because  the trip started and finished at the same station,
#### 2.	The “Gender Sensitivity” issue; so called due to people’s reluctance to disclose gender. 

These have been explored and summarised below.

### The “Lap Trips” Phenomenon 

The highlight of this phenomenon is that 15.5% of all trips (209,476) started and ended at the same station. Of these trips 6,776 trips were of 1- or 2-minutes duration indicating that the bikes were returned almost immediately perhaps due to a fault and that the trip had no useful outcome. The remainder of these trips varied from 3 minutes to 22 days duration. It would be useful to analyse these trips further, but data constraints and time preclude that analysis at this stage. 
   
 
#### The “Gender Sensitivity” Phenomenon
Males typically use CitiBikes 2-3 times more than females. The characteristics of their respective trips are similar in terms of average trip duration, average trip speed and, as a corollary of this average trip distance. 

The significant aspect of what I have called the “Gender Sensitivity” Phenomenon is the high proportion of trips where gender is unknown. This highlights peoples’ reluctance to disclose their gender perhaps due to sensitivity regarding gender disclosure and / or perhaps due to privacy / identity concerns. 

Analysis of trip patterns by season shows that trip durations peak in April and taper off in the warmer months. Average speeds are faster in January and February and also taper off in the warmer months.

Summer trip patterns show a gradual increase in trips throughout the day starting at 7AM with a huge peak between 6PM and 8PM. Since covid lock downs, walking and cycling have become more popular forms of exercise as they are less risky than other forms requiring close contact with other people. This may account for the huge evening peak, but further analysis needs to be done to confirm this. 

In Winter there are predictable morning (8AM) and evening (5-6PM) peaks for trips. These coincide with commuters going to and returning from work. 
 
 
### The Other Visualisations Required for the Assignment
### Dashboards
In addition to the “Lap Trip” and the “Gender Sensitivity” Dashboards, the following dashboard was created to show the top ranked start and end stations and the bottom ranked start and end stations.
  

 
A “Tale of Two CitiBikes Phenomena for Jersey City” 
This Story Board was created to provide an overview of the program.
 
 
 

 

 

 

 

 

 


